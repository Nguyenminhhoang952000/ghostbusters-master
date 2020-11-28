# ghostbusters-master
Câu 1: Triển khai cập nhập niềm tin của pacman dựa trên quan sát của pacman
+ Xác định được vị trị đầu tiên chúng ta sẽ kiểm tra xem có con ma nào bị bắt chưa qua bằng noisyDistance == None.
+Sử dụng vòng lặp for để đi qua tất cả các vị trí mà con ma có thể xuất hiện sử dụng khoảng cách manhattanDistance để tính khoảng cách của pacman và các vị trí sau đó và cập nhập lại niềm tin sau khi bắt được mà.
sự xuất hiện của các ô màu , ô màu càng sáng thì vị trí ở gần con ma càng rõ nét , ô màu nhạt hơn thì vị trí kém xuất hiện hơn của con ma dựa trên quan sát của pacman
Câu 2: Sử dụng Time Elapse triển khai cập nhập niềm tin cho pacman dựa trên kiến thức di chuyển của pacman là ma thì không đi xuyên được qua tường và nhiều khoảng trống trong 1 bước thời gian 
+ Triển khai cập nhập niềm tin bằng cách đi qua vòng lặp for đi qua legalPositions ( là tất cả các vị trí của con ma)
+ newPosDist: ứng với mỗi p trong vòng lặp sẽ thể hiện vị trí mới của con ma sau đó sẽ cập nhập lại niềm tin 
Câu 3: Nhiệm vụ của chúng ta la kết hợp cả việc quan sát pacman và cả kiến thức có sẵn về việc di chuyển của con ma và sự quan sát của pacman để cài đặt 
+ livingGhostPositionDistributions : danh sách các niềm tin vị trí phân phối của từng con ma vẫn còn sống , pacmanPosition vị trí hiện tại của pacman 
+ Có thể nhìn thấy xung quanh con ma có ô màu đậm hơn là vị trí rõ ràng của con ma, ô nhạt hơn thì tầm quan sát của pacman nhiều hơn
Câu 4: Hoàn thành các chức năng initializeUniformly, getBeliefDistribution , and observe  trong lớp ParticleFilter 
+ Đối với hàm initializeUniformly -- khởi tạo danh sách các hàm và cài đặt các hàm vào trong vị trí 
+ Đối với hàm observe-- cập nhập niềm tin . Nếu pacman ăn ma thì vị trí hat la vị trí tu của ma nếu không thì niềm tin sẽ được cập nhập theo trueDistance
+ Thấy được vị trí các hạt khi di chuyển các hạt cũng sẽ được cập nhập 
Câu 5: Sử dụng Time Elapse .Cài đặt elapseTime
+ Sử dụng vòng lặp để lấy ra vị trí của tất cả các con ma
+ Rồi sẽ lấy mẫu 1 số vị trí của các hạt 
+ Thêm newPosDist vào trong newParticles ( 1 hạt mới) 
