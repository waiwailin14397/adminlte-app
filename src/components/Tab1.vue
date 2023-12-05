<template>
	<!-- Content Wrapper. Contains page content -->
	<div class="content-wrapper">
	<!-- Content Header (Page header) -->
	<div class="container-fluid">
	  <div class="row mb-2">
		<div class="col-md-12 col-sm-12 col-12">
		  <h2><i class="fas fa-edit"></i> Tab1 </h2>
		</div>
	  </div>
	</div>
	  <!-- Main content -->
	  <div class="content">
		<div class="container-fluid k_header">
		  <div class="col-md-12 col-sm-12 col-12">
			<div class="info-box shadow  mt-4">
			  <span class="info-box-icon bg-warning">
				<i class="fas fa-wrench"></i>
			  </span>
			  <div class="info-box-content">
				<span class="info-box-text text-sm">
				  <div class="container-fluid">
					<div class="row">
					  <div class="col-sm-auto"><b>【件名】</b> <p v-if="message">{{ message }}</p> </div>
					</div>
				  </div>
				</span>
			  </div>
			  <!-- /.info-box-content -->
			</div>
			<!-- /.info-box -->
		  </div>
		  <!-- /.container-fluid -->
		</div>
		<!-- /.container-fluid -->
	  </div>
	  <!-- /.content -->
	</div>
	<!-- /.content-wrapper -->
  </template>
  
  <script>
//   export default {
//     data() {
// 		return {
// 			message: "",
// 			error: ""
// 		};
// 	},
// 	mounted() {
// 		liff
// 		.init({
// 			liffId: import.meta.env.VITE_LIFF_ID
// 		})
// 		.then(() => {
// 			this.message = "LIFF init succeeded.";
// 		})
// 		.catch((e) => {
// 			this.message = "LIFF init failed.";
// 			this.error = `${e}`;
// 		});
// 	}
// }
  </script>
  
  <style>
  /* */
  </style>
  