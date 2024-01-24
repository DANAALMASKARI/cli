package com.my.newproject;

import android.Manifest;
import android.animation.*;
import android.app.*;
import android.content.*;
import android.content.ClipData;
import android.content.Intent;
import android.content.pm.PackageManager;
import android.content.res.*;
import android.graphics.*;
import android.graphics.drawable.*;
import android.media.*;
import android.net.*;
import android.net.Uri;
import android.os.*;
import android.text.*;
import android.text.style.*;
import android.util.*;
import android.view.*;
import android.view.View;
import android.view.View.*;
import android.view.animation.*;
import android.webkit.*;
import android.widget.*;
import android.widget.EditText;
import android.widget.HorizontalScrollView;
import android.widget.ImageView;
import android.widget.LinearLayout;
import android.widget.ScrollView;
import android.widget.TextView;
import androidx.annotation.*;
import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.widget.Toolbar;
import androidx.cardview.widget.CardView;
import androidx.coordinatorlayout.widget.CoordinatorLayout;
import androidx.core.app.ActivityCompat;
import androidx.core.content.ContextCompat;
import androidx.fragment.app.DialogFragment;
import androidx.fragment.app.Fragment;
import androidx.fragment.app.FragmentManager;
import com.google.android.gms.tasks.Continuation;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.OnFailureListener;
import com.google.android.gms.tasks.OnSuccessListener;
import com.google.android.gms.tasks.Task;
import com.google.android.material.appbar.AppBarLayout;
import com.google.android.material.floatingactionbutton.FloatingActionButton;
import com.google.firebase.FirebaseApp;
import com.google.firebase.auth.AuthResult;
import com.google.firebase.auth.FirebaseAuth;
import com.google.firebase.auth.FirebaseUser;
import com.google.firebase.database.ChildEventListener;
import com.google.firebase.database.DataSnapshot;
import com.google.firebase.database.DatabaseError;
import com.google.firebase.database.DatabaseReference;
import com.google.firebase.database.FirebaseDatabase;
import com.google.firebase.database.GenericTypeIndicator;
import com.google.firebase.database.ValueEventListener;
import com.google.firebase.storage.FileDownloadTask;
import com.google.firebase.storage.FirebaseStorage;
import com.google.firebase.storage.OnProgressListener;
import com.google.firebase.storage.StorageReference;
import com.google.firebase.storage.UploadTask;
import java.io.*;
import java.io.File;
import java.text.*;
import java.util.*;
import java.util.HashMap;
import java.util.regex.*;
import org.json.*;

public class AddActivity extends AppCompatActivity {
      
      public final int REQ_CD_IMGMAIN = 101;
      public final int REQ_CD_IMG1 = 102;
      public final int REQ_CD_IMG2 = 103;
      public final int REQ_CD_IMG3 = 104;
      public final int REQ_CD_IMG4 = 105;
      
      private FirebaseDatabase _firebase = FirebaseDatabase.getInstance();
      private FirebaseStorage _firebase_storage = FirebaseStorage.getInstance();
      
      private Toolbar _toolbar;
      private AppBarLayout _app_bar;
      private CoordinatorLayout _coordinator;
      private FloatingActionButton _fab;
      private String fontName = "";
      private String typeace = "";
      private String str_main_img = "";
      private String str_img1 = "";
      private String str_img2 = "";
      private String str_img3 = "";
      private String str_img4 = "";
      private String str_main_img_url = "";
      private String str_main_1_url = "";
      private String str_main_2_url = "";
      private String str_main_4_url = "";
      private String str_main_3_url = "";
      private HashMap<String, Object> mv = new HashMap<>();
      private String key = "";
      private String name = "";
      
      private LinearLayout lin_bg;
      private ScrollView vscroll1;
      private LinearLayout linear1;
      private TextView textview1;
      private CardView cardview1;
      private LinearLayout linear2;
      private LinearLayout location1;
      private LinearLayout location2;
      private EditText edittext3;
      private EditText edittextCall;
      private EditText edittextWA;
      private TextView textview3;
      private TextView textview2;
      private HorizontalScrollView hscroll1;
      private ImageView product;
      private EditText edittext1;
      private EditText edittext2;
      private EditText location;
      private ImageView imageview5;
      private EditText from;
      private EditText to;
      private LinearLayout linear3;
      private CardView img_product1;
      private CardView img_product2;
      private CardView img_product3;
      private CardView img_product4;
      private ImageView imageview1;
      private ImageView imageview2;
      private ImageView imageview3;
      private ImageView imageview4;
      
      private Intent IMGMain = new Intent(Intent.ACTION_GET_CONTENT);
      private Intent img1 = new Intent(Intent.ACTION_GET_CONTENT);
      private Intent img2 = new Intent(Intent.ACTION_GET_CONTENT);
      private Intent img3 = new Intent(Intent.ACTION_GET_CONTENT);
      private Intent img4 = new Intent(Intent.ACTION_GET_CONTENT);
      private StorageReference fs_mian_img = _firebase_storage.getReference("fs_mian_img");
      private OnCompleteListener<Uri> _fs_mian_img_upload_success_listener;
      private OnSuccessListener<FileDownloadTask.TaskSnapshot> _fs_mian_img_download_success_listener;
      private OnSuccessListener _fs_mian_img_delete_success_listener;
      private OnProgressListener _fs_mian_img_upload_progress_listener;
      private OnProgressListener _fs_mian_img_download_progress_listener;
      private OnFailureListener _fs_mian_img_failure_listener;
      
      private StorageReference fs_img1 = _firebase_storage.getReference("fs_img1");
      private OnCompleteListener<Uri> _fs_img1_upload_success_listener;
      private OnSuccessListener<FileDownloadTask.TaskSnapshot> _fs_img1_download_success_listener;
      private OnSuccessListener _fs_img1_delete_success_listener;
      private OnProgressListener _fs_img1_upload_progress_listener;
      private OnProgressListener _fs_img1_download_progress_listener;
      private OnFailureListener _fs_img1_failure_listener;
      
      private StorageReference fs_img2 = _firebase_storage.getReference("fs_img2");
      private OnCompleteListener<Uri> _fs_img2_upload_success_listener;
      private OnSuccessListener<FileDownloadTask.TaskSnapshot> _fs_img2_download_success_listener;
      private OnSuccessListener _fs_img2_delete_success_listener;
      private OnProgressListener _fs_img2_upload_progress_listener;
      private OnProgressListener _fs_img2_download_progress_listener;
      private OnFailureListener _fs_img2_failure_listener;
      
      private StorageReference fs_img3 = _firebase_storage.getReference("fs_img3");
      private OnCompleteListener<Uri> _fs_img3_upload_success_listener;
      private OnSuccessListener<FileDownloadTask.TaskSnapshot> _fs_img3_download_success_listener;
      private OnSuccessListener _fs_img3_delete_success_listener;
      private OnProgressListener _fs_img3_upload_progress_listener;
      private OnProgressListener _fs_img3_download_progress_listener;
      private OnFailureListener _fs_img3_failure_listener;
      
      private StorageReference fs_img4 = _firebase_storage.getReference("fs_img4");
      private OnCompleteListener<Uri> _fs_img4_upload_success_listener;
      private OnSuccessListener<FileDownloadTask.TaskSnapshot> _fs_img4_download_success_listener;
      private OnSuccessListener _fs_img4_delete_success_listener;
      private OnProgressListener _fs_img4_upload_progress_listener;
      private OnProgressListener _fs_img4_download_progress_listener;
      private OnFailureListener _fs_img4_failure_listener;
      
      private FirebaseAuth authUser;
      private OnCompleteListener<AuthResult> _authUser_create_user_listener;
      private OnCompleteListener<AuthResult> _authUser_sign_in_listener;
      private OnCompleteListener<Void> _authUser_reset_password_listener;
      private OnCompleteListener<Void> authUser_updateEmailListener;
      private OnCompleteListener<Void> authUser_updatePasswordListener;
      private OnCompleteListener<Void> authUser_emailVerificationSentListener;
      private OnCompleteListener<Void> authUser_deleteUserListener;
      private OnCompleteListener<Void> authUser_updateProfileListener;
      private OnCompleteListener<AuthResult> authUser_phoneAuthListener;
      private OnCompleteListener<AuthResult> authUser_googleSignInListener;
      
      private DatabaseReference DBUser = _firebase.getReference("DBUser");
      private ChildEventListener _DBUser_child_listener;
      private DatabaseReference DB_items2 = _firebase.getReference("DB_items2");
      private ChildEventListener _DB_items2_child_listener;
      private DatabaseReference DB_items1 = _firebase.getReference("DB_items1");
      private ChildEventListener _DB_items1_child_listener;
      
      @Override
      protected void onCreate(Bundle _savedInstanceState) {
            super.onCreate(_savedInstanceState);
            setContentView(R.layout.add);
            initialize(_savedInstanceState);
            FirebaseApp.initializeApp(this);
            
            if (ContextCompat.checkSelfPermission(this, Manifest.permission.READ_EXTERNAL_STORAGE) == PackageManager.PERMISSION_DENIED
            || ContextCompat.checkSelfPermission(this, Manifest.permission.WRITE_EXTERNAL_STORAGE) == PackageManager.PERMISSION_DENIED) {
                  ActivityCompat.requestPermissions(this, new String[] {Manifest.permission.READ_EXTERNAL_STORAGE, Manifest.permission.WRITE_EXTERNAL_STORAGE}, 1000);
            } else {
                  initializeLogic();
            }
      }
      
      @Override
      public void onRequestPermissionsResult(int requestCode, String[] permissions, int[] grantResults) {
            super.onRequestPermissionsResult(requestCode, permissions, grantResults);
            if (requestCode == 1000) {
                  initializeLogic();
            }
      }
      
      private void initialize(Bundle _savedInstanceState) {
            _app_bar = findViewById(R.id._app_bar);
            _coordinator = findViewById(R.id._coordinator);
            _toolbar = findViewById(R.id._toolbar);
            setSupportActionBar(_toolbar);
            getSupportActionBar().setDisplayHomeAsUpEnabled(true);
            getSupportActionBar().setHomeButtonEnabled(true);
            _toolbar.setNavigationOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _v) {
                        onBackPressed();
                  }
            });
            _fab = findViewById(R.id._fab);
            
            lin_bg = findViewById(R.id.lin_bg);
            vscroll1 = findViewById(R.id.vscroll1);
            linear1 = findViewById(R.id.linear1);
            textview1 = findViewById(R.id.textview1);
            cardview1 = findViewById(R.id.cardview1);
            linear2 = findViewById(R.id.linear2);
            location1 = findViewById(R.id.location1);
            location2 = findViewById(R.id.location2);
            edittext3 = findViewById(R.id.edittext3);
            edittextCall = findViewById(R.id.edittextCall);
            edittextWA = findViewById(R.id.edittextWA);
            textview3 = findViewById(R.id.textview3);
            textview2 = findViewById(R.id.textview2);
            hscroll1 = findViewById(R.id.hscroll1);
            product = findViewById(R.id.product);
            edittext1 = findViewById(R.id.edittext1);
            edittext2 = findViewById(R.id.edittext2);
            location = findViewById(R.id.location);
            imageview5 = findViewById(R.id.imageview5);
            from = findViewById(R.id.from);
            to = findViewById(R.id.to);
            linear3 = findViewById(R.id.linear3);
            img_product1 = findViewById(R.id.img_product1);
            img_product2 = findViewById(R.id.img_product2);
            img_product3 = findViewById(R.id.img_product3);
            img_product4 = findViewById(R.id.img_product4);
            imageview1 = findViewById(R.id.imageview1);
            imageview2 = findViewById(R.id.imageview2);
            imageview3 = findViewById(R.id.imageview3);
            imageview4 = findViewById(R.id.imageview4);
            IMGMain.setType("image/*");
            IMGMain.putExtra(Intent.EXTRA_ALLOW_MULTIPLE, true);
            img1.setType("image/*");
            img1.putExtra(Intent.EXTRA_ALLOW_MULTIPLE, true);
            img2.setType("image/*");
            img2.putExtra(Intent.EXTRA_ALLOW_MULTIPLE, true);
            img3.setType("image/*");
            img3.putExtra(Intent.EXTRA_ALLOW_MULTIPLE, true);
            img4.setType("image/*");
            img4.putExtra(Intent.EXTRA_ALLOW_MULTIPLE, true);
            authUser = FirebaseAuth.getInstance();
            
            cardview1.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _view) {
                        startActivityForResult(IMGMain, REQ_CD_IMGMAIN);
                  }
            });
            
            img_product1.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _view) {
                        
                  }
            });
            
            img_product2.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _view) {
                        
                  }
            });
            
            img_product3.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _view) {
                        
                  }
            });
            
            img_product4.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _view) {
                        
                  }
            });
            
            _fab.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View _view) {
                        if (str_main_img.equals("")) {
                              SketchwareUtil.showMessage(getApplicationContext(), "Main image empty");
                        }
                        else {
                              if (edittext1.getText().toString().equals("")) {
                                    SketchwareUtil.showMessage(getApplicationContext(), "Name product empty");
                              }
                              else {
                                    if (edittext2.getText().toString().equals("")) {
                                          SketchwareUtil.showMessage(getApplicationContext(), "price empty");
                                    }
                                    else {
                                          if (edittext3.getText().toString().equals("")) {
                                                SketchwareUtil.showMessage(getApplicationContext(), "Description empty");
                                          }
                                          else {
                                                if (edittextCall.getText().toString().equals("")) {
                                                      SketchwareUtil.showMessage(getApplicationContext(), "Phone Number empty");
                                                }
                                                else {
                                                      if (str_img1.equals("")) {
                                                            SketchwareUtil.showMessage(getApplicationContext(), "Image product empty");
                                                      }
                                                      else {
                                                            fs_mian_img.child(Uri.parse(str_main_img).getLastPathSegment()).putFile(Uri.fromFile(new File(str_main_img))).addOnFailureListener(_fs_mian_img_failure_listener).addOnProgressListener(_fs_mian_img_upload_progress_listener).continueWithTask(new Continuation<UploadTask.TaskSnapshot, Task<Uri>>() {
                                                                  @Override
                                                                  public Task<Uri> then(Task<UploadTask.TaskSnapshot> task) throws Exception {
                                                                        return fs_mian_img.child(Uri.parse(str_main_img).getLastPathSegment()).getDownloadUrl();
                                                                  }}).addOnCompleteListener(_fs_mian_img_upload_success_listener);
                                                            _Prog_Dialogue_show(true, "", "Loading... ");
                                                      }
                                                }
                                          }
                                    }
                              }
                        }
                  }
            });
            
            _fs_mian_img_upload_progress_listener = new OnProgressListener<UploadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(UploadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        _Prog_Dialogue_show(true, "", "Uploading main image".concat(String.valueOf((long)(_progressValue))));
                  }
            };
            
            _fs_mian_img_download_progress_listener = new OnProgressListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(FileDownloadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_mian_img_upload_success_listener = new OnCompleteListener<Uri>() {
                  @Override
                  public void onComplete(Task<Uri> _param1) {
                        final String _downloadUrl = _param1.getResult().toString();
                        _Prog_Dialogue_show(false, "", "");
                        str_main_img_url = _downloadUrl;
                        fs_img1.child(Uri.parse(str_img1).getLastPathSegment()).putFile(Uri.fromFile(new File(str_img1))).addOnFailureListener(_fs_img1_failure_listener).addOnProgressListener(_fs_img1_upload_progress_listener).continueWithTask(new Continuation<UploadTask.TaskSnapshot, Task<Uri>>() {
                              @Override
                              public Task<Uri> then(Task<UploadTask.TaskSnapshot> task) throws Exception {
                                    return fs_img1.child(Uri.parse(str_img1).getLastPathSegment()).getDownloadUrl();
                              }}).addOnCompleteListener(_fs_img1_upload_success_listener);
                  }
            };
            
            _fs_mian_img_download_success_listener = new OnSuccessListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onSuccess(FileDownloadTask.TaskSnapshot _param1) {
                        final long _totalByteCount = _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_mian_img_delete_success_listener = new OnSuccessListener() {
                  @Override
                  public void onSuccess(Object _param1) {
                        
                  }
            };
            
            _fs_mian_img_failure_listener = new OnFailureListener() {
                  @Override
                  public void onFailure(Exception _param1) {
                        final String _message = _param1.getMessage();
                        
                  }
            };
            
            _fs_img1_upload_progress_listener = new OnProgressListener<UploadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(UploadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        _Prog_Dialogue_show(true, "", "Uploading image... ".concat(String.valueOf((long)(_progressValue))));
                  }
            };
            
            _fs_img1_download_progress_listener = new OnProgressListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(FileDownloadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img1_upload_success_listener = new OnCompleteListener<Uri>() {
                  @Override
                  public void onComplete(Task<Uri> _param1) {
                        final String _downloadUrl = _param1.getResult().toString();
                        _Prog_Dialogue_show(false, "", "");
                        str_main_1_url = _downloadUrl;
                        if (str_img2.equals("")) {
                              mv = new HashMap<>();
                              key = DBUser.push().getKey();
                              mv.put("key", key);
                              mv.put("main_img", str_main_img_url);
                              mv.put("Img1", str_main_1_url);
                              mv.put("Img2", str_main_2_url);
                              mv.put("Img3", str_main_3_url);
                              mv.put("Img4", str_main_4_url);
                              mv.put("OwnerProduct", name);
                              mv.put("ProductItem", getIntent().getStringExtra("item"));
                              mv.put("call", edittextCall.getText().toString());
                              mv.put("WA", edittextWA.getText().toString());
                              mv.put("name", edittext1.getText().toString());
                              mv.put("price", edittext2.getText().toString());
                              mv.put("description", edittext3.getText().toString());
                              mv.put("Location", location.getText().toString());
                              mv.put("uid", FirebaseAuth.getInstance().getCurrentUser().getUid());
                              if (getIntent().getStringExtra("item").equals("Hotel")) {
                                    mv.put("Location", location.getText().toString());
                                    DB_items1.child(key).updateChildren(mv);
                              }
                              else {
                                    mv.put("Location_from", from.getText().toString());
                                    mv.put("Location_to", to.getText().toString());
                                    DB_items2.child(key).updateChildren(mv);
                              }
                              mv.clear();
                              _empty();
                        }
                        else {
                              fs_img2.child(Uri.parse(str_img2).getLastPathSegment()).putFile(Uri.fromFile(new File(str_img2))).addOnFailureListener(_fs_img2_failure_listener).addOnProgressListener(_fs_img2_upload_progress_listener).continueWithTask(new Continuation<UploadTask.TaskSnapshot, Task<Uri>>() {
                                    @Override
                                    public Task<Uri> then(Task<UploadTask.TaskSnapshot> task) throws Exception {
                                          return fs_img2.child(Uri.parse(str_img2).getLastPathSegment()).getDownloadUrl();
                                    }}).addOnCompleteListener(_fs_img2_upload_success_listener);
                        }
                  }
            };
            
            _fs_img1_download_success_listener = new OnSuccessListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onSuccess(FileDownloadTask.TaskSnapshot _param1) {
                        final long _totalByteCount = _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img1_delete_success_listener = new OnSuccessListener() {
                  @Override
                  public void onSuccess(Object _param1) {
                        
                  }
            };
            
            _fs_img1_failure_listener = new OnFailureListener() {
                  @Override
                  public void onFailure(Exception _param1) {
                        final String _message = _param1.getMessage();
                        
                  }
            };
            
            _fs_img2_upload_progress_listener = new OnProgressListener<UploadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(UploadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        _Prog_Dialogue_show(true, "", "Uploading image... ".concat(String.valueOf((long)(_progressValue))));
                  }
            };
            
            _fs_img2_download_progress_listener = new OnProgressListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(FileDownloadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img2_upload_success_listener = new OnCompleteListener<Uri>() {
                  @Override
                  public void onComplete(Task<Uri> _param1) {
                        final String _downloadUrl = _param1.getResult().toString();
                        _Prog_Dialogue_show(false, "", "");
                        str_main_2_url = _downloadUrl;
                        if (str_img3.equals("")) {
                              mv = new HashMap<>();
                              key = DBUser.push().getKey();
                              mv.put("key", key);
                              mv.put("main_img", str_main_img_url);
                              mv.put("Img1", str_main_1_url);
                              mv.put("Img2", str_main_2_url);
                              mv.put("Img3", str_main_3_url);
                              mv.put("Img4", str_main_4_url);
                              mv.put("OwnerProduct", name);
                              mv.put("ProductItem", getIntent().getStringExtra("item"));
                              mv.put("call", edittextCall.getText().toString());
                              mv.put("WA", edittextWA.getText().toString());
                              mv.put("name", edittext1.getText().toString());
                              mv.put("price", edittext2.getText().toString());
                              mv.put("description", edittext3.getText().toString());
                              mv.put("Location", location.getText().toString());
                              mv.put("uid", FirebaseAuth.getInstance().getCurrentUser().getUid());
                              if (getIntent().getStringExtra("item").equals("Hotel")) {
                                    mv.put("Location", location.getText().toString());
                                    DB_items1.child(key).updateChildren(mv);
                              }
                              else {
                                    mv.put("Location_from", from.getText().toString());
                                    mv.put("Location_to", to.getText().toString());
                                    DB_items2.child(key).updateChildren(mv);
                              }
                              mv.clear();
                              _empty();
                        }
                        else {
                              fs_img3.child(Uri.parse(str_img3).getLastPathSegment()).putFile(Uri.fromFile(new File(str_img3))).addOnFailureListener(_fs_img3_failure_listener).addOnProgressListener(_fs_img3_upload_progress_listener).continueWithTask(new Continuation<UploadTask.TaskSnapshot, Task<Uri>>() {
                                    @Override
                                    public Task<Uri> then(Task<UploadTask.TaskSnapshot> task) throws Exception {
                                          return fs_img3.child(Uri.parse(str_img3).getLastPathSegment()).getDownloadUrl();
                                    }}).addOnCompleteListener(_fs_img3_upload_success_listener);
                        }
                  }
            };
            
            _fs_img2_download_success_listener = new OnSuccessListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onSuccess(FileDownloadTask.TaskSnapshot _param1) {
                        final long _totalByteCount = _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img2_delete_success_listener = new OnSuccessListener() {
                  @Override
                  public void onSuccess(Object _param1) {
                        
                  }
            };
            
            _fs_img2_failure_listener = new OnFailureListener() {
                  @Override
                  public void onFailure(Exception _param1) {
                        final String _message = _param1.getMessage();
                        
                  }
            };
            
            _fs_img3_upload_progress_listener = new OnProgressListener<UploadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(UploadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        _Prog_Dialogue_show(true, "", "Uploading image...".concat(String.valueOf((long)(_progressValue))));
                  }
            };
            
            _fs_img3_download_progress_listener = new OnProgressListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(FileDownloadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img3_upload_success_listener = new OnCompleteListener<Uri>() {
                  @Override
                  public void onComplete(Task<Uri> _param1) {
                        final String _downloadUrl = _param1.getResult().toString();
                        _Prog_Dialogue_show(false, "", "");
                        str_main_3_url = _downloadUrl;
                        if (str_img4.equals("")) {
                              mv = new HashMap<>();
                              key = DBUser.push().getKey();
                              mv.put("key", key);
                              mv.put("main_img", str_main_img_url);
                              mv.put("Img1", str_main_1_url);
                              mv.put("Img2", str_main_2_url);
                              mv.put("Img3", str_main_3_url);
                              mv.put("Img4", str_main_4_url);
                              mv.put("OwnerProduct", name);
                              mv.put("ProductItem", getIntent().getStringExtra("item"));
                              mv.put("call", edittextCall.getText().toString());
                              mv.put("WA", edittextWA.getText().toString());
                              mv.put("name", edittext1.getText().toString());
                              mv.put("price", edittext2.getText().toString());
                              mv.put("description", edittext3.getText().toString());
                              mv.put("Location", location.getText().toString());
                              mv.put("uid", FirebaseAuth.getInstance().getCurrentUser().getUid());
                              if (getIntent().getStringExtra("item").equals("Hotel")) {
                                    mv.put("Location", location.getText().toString());
                                    DB_items1.child(key).updateChildren(mv);
                              }
                              else {
                                    mv.put("Location_from", from.getText().toString());
                                    mv.put("Location_to", to.getText().toString());
                                    DB_items2.child(key).updateChildren(mv);
                              }
                              mv.clear();
                              _empty();
                        }
                        else {
                              fs_img4.child(Uri.parse(str_img4).getLastPathSegment()).putFile(Uri.fromFile(new File(str_img4))).addOnFailureListener(_fs_img4_failure_listener).addOnProgressListener(_fs_img4_upload_progress_listener).continueWithTask(new Continuation<UploadTask.TaskSnapshot, Task<Uri>>() {
                                    @Override
                                    public Task<Uri> then(Task<UploadTask.TaskSnapshot> task) throws Exception {
                                          return fs_img4.child(Uri.parse(str_img4).getLastPathSegment()).getDownloadUrl();
                                    }}).addOnCompleteListener(_fs_img4_upload_success_listener);
                        }
                  }
            };
            
            _fs_img3_download_success_listener = new OnSuccessListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onSuccess(FileDownloadTask.TaskSnapshot _param1) {
                        final long _totalByteCount = _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img3_delete_success_listener = new OnSuccessListener() {
                  @Override
                  public void onSuccess(Object _param1) {
                        
                  }
            };
            
            _fs_img3_failure_listener = new OnFailureListener() {
                  @Override
                  public void onFailure(Exception _param1) {
                        final String _message = _param1.getMessage();
                        
                  }
            };
            
            _fs_img4_upload_progress_listener = new OnProgressListener<UploadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(UploadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        _Prog_Dialogue_show(true, "", "Uploading image... ".concat(String.valueOf((long)(_progressValue))));
                  }
            };
            
            _fs_img4_download_progress_listener = new OnProgressListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onProgress(FileDownloadTask.TaskSnapshot _param1) {
                        double _progressValue = (100.0 * _param1.getBytesTransferred()) / _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img4_upload_success_listener = new OnCompleteListener<Uri>() {
                  @Override
                  public void onComplete(Task<Uri> _param1) {
                        final String _downloadUrl = _param1.getResult().toString();
                        _Prog_Dialogue_show(false, "", "");
                        str_main_4_url = _downloadUrl;
                        mv = new HashMap<>();
                        key = DBUser.push().getKey();
                        mv.put("key", key);
                        mv.put("main_img", str_main_img_url);
                        mv.put("Img1", str_main_1_url);
                        mv.put("Img2", str_main_2_url);
                        mv.put("Img3", str_main_3_url);
                        mv.put("Img4", str_main_4_url);
                        mv.put("OwnerProduct", name);
                        mv.put("ProductItem", getIntent().getStringExtra("item"));
                        mv.put("call", edittextCall.getText().toString());
                        mv.put("WA", edittextWA.getText().toString());
                        mv.put("name", edittext1.getText().toString());
                        mv.put("price", edittext2.getText().toString());
                        mv.put("description", edittext3.getText().toString());
                        mv.put("uid", FirebaseAuth.getInstance().getCurrentUser().getUid());
                        if (getIntent().getStringExtra("item").equals("Hotel")) {
                              mv.put("Location", location.getText().toString());
                              DB_items1.child(key).updateChildren(mv);
                        }
                        else {
                              mv.put("Location_from", to.getText().toString());
                              mv.put("Location_to", from.getText().toString());
                              DB_items2.child(key).updateChildren(mv);
                        }
                        mv.clear();
                        _empty();
                  }
            };
            
            _fs_img4_download_success_listener = new OnSuccessListener<FileDownloadTask.TaskSnapshot>() {
                  @Override
                  public void onSuccess(FileDownloadTask.TaskSnapshot _param1) {
                        final long _totalByteCount = _param1.getTotalByteCount();
                        
                  }
            };
            
            _fs_img4_delete_success_listener = new OnSuccessListener() {
                  @Override
                  public void onSuccess(Object _param1) {
                        
                  }
            };
            
            _fs_img4_failure_listener = new OnFailureListener() {
                  @Override
                  public void onFailure(Exception _param1) {
                        final String _message = _param1.getMessage();
                        
                  }
            };
            
            _DBUser_child_listener = new ChildEventListener() {
                  @Override
                  public void onChildAdded(DataSnapshot _param1, String _param2) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        if (_childKey.equals(FirebaseAuth.getInstance().getCurrentUser().getUid())) {
                              if (_childValue.containsKey("name")) {
                                    name = _childValue.get("name").toString();
                              }
                        }
                  }
                  
                  @Override
                  public void onChildChanged(DataSnapshot _param1, String _param2) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onChildMoved(DataSnapshot _param1, String _param2) {
                        
                  }
                  
                  @Override
                  public void onChildRemoved(DataSnapshot _param1) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onCancelled(DatabaseError _param1) {
                        final int _errorCode = _param1.getCode();
                        final String _errorMessage = _param1.getMessage();
                        
                  }
            };
            DBUser.addChildEventListener(_DBUser_child_listener);
            
            _DB_items2_child_listener = new ChildEventListener() {
                  @Override
                  public void onChildAdded(DataSnapshot _param1, String _param2) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onChildChanged(DataSnapshot _param1, String _param2) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onChildMoved(DataSnapshot _param1, String _param2) {
                        
                  }
                  
                  @Override
                  public void onChildRemoved(DataSnapshot _param1) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onCancelled(DatabaseError _param1) {
                        final int _errorCode = _param1.getCode();
                        final String _errorMessage = _param1.getMessage();
                        
                  }
            };
            DB_items2.addChildEventListener(_DB_items2_child_listener);
            
            _DB_items1_child_listener = new ChildEventListener() {
                  @Override
                  public void onChildAdded(DataSnapshot _param1, String _param2) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onChildChanged(DataSnapshot _param1, String _param2) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onChildMoved(DataSnapshot _param1, String _param2) {
                        
                  }
                  
                  @Override
                  public void onChildRemoved(DataSnapshot _param1) {
                        GenericTypeIndicator<HashMap<String, Object>> _ind = new GenericTypeIndicator<HashMap<String, Object>>() {};
                        final String _childKey = _param1.getKey();
                        final HashMap<String, Object> _childValue = _param1.getValue(_ind);
                        
                  }
                  
                  @Override
                  public void onCancelled(DatabaseError _param1) {
                        final int _errorCode = _param1.getCode();
                        final String _errorMessage = _param1.getMessage();
                        
                  }
            };
            DB_items1.addChildEventListener(_DB_items1_child_listener);
            
            authUser_updateEmailListener = new OnCompleteListener<Void>() {
                  @Override
                  public void onComplete(Task<Void> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            authUser_updatePasswordListener = new OnCompleteListener<Void>() {
                  @Override
                  public void onComplete(Task<Void> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            authUser_emailVerificationSentListener = new OnCompleteListener<Void>() {
                  @Override
                  public void onComplete(Task<Void> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            authUser_deleteUserListener = new OnCompleteListener<Void>() {
                  @Override
                  public void onComplete(Task<Void> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            authUser_phoneAuthListener = new OnCompleteListener<AuthResult>() {
                  @Override
                  public void onComplete(Task<AuthResult> task) {
                        final boolean _success = task.isSuccessful();
                        final String _errorMessage = task.getException() != null ? task.getException().getMessage() : "";
                        
                  }
            };
            
            authUser_updateProfileListener = new OnCompleteListener<Void>() {
                  @Override
                  public void onComplete(Task<Void> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            authUser_googleSignInListener = new OnCompleteListener<AuthResult>() {
                  @Override
                  public void onComplete(Task<AuthResult> task) {
                        final boolean _success = task.isSuccessful();
                        final String _errorMessage = task.getException() != null ? task.getException().getMessage() : "";
                        
                  }
            };
            
            _authUser_create_user_listener = new OnCompleteListener<AuthResult>() {
                  @Override
                  public void onComplete(Task<AuthResult> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            _authUser_sign_in_listener = new OnCompleteListener<AuthResult>() {
                  @Override
                  public void onComplete(Task<AuthResult> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        final String _errorMessage = _param1.getException() != null ? _param1.getException().getMessage() : "";
                        
                  }
            };
            
            _authUser_reset_password_listener = new OnCompleteListener<Void>() {
                  @Override
                  public void onComplete(Task<Void> _param1) {
                        final boolean _success = _param1.isSuccessful();
                        
                  }
            };
      }
      
      private void initializeLogic() {
            _changeActivityFont("tajawal_bold");
            setTitle(getIntent().getStringExtra("item"));
            img_product2.setVisibility(View.GONE);
            img_product3.setVisibility(View.GONE);
            img_product4.setVisibility(View.GONE);
            edittextWA.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            edittextCall.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            edittext3.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            edittext2.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            edittext1.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            from.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            to.setBackground(new GradientDrawable() { public GradientDrawable getIns(int a, int b) { this.setCornerRadius(a); this.setColor(b); return this; } }.getIns((int)30, 0xFFEEEEEE));
            img_product1.setOnClickListener(new View.OnClickListener() {
                        @Override
                        public void onClick(View _view) {
                                    startActivityForResult(img1, REQ_CD_IMG1);
                        }
            });
            img_product2.setOnClickListener(new View.OnClickListener() {
                        @Override
                        public void onClick(View _view) {
                                    startActivityForResult(img2, REQ_CD_IMG2);
                        }
            });
            img_product3.setOnClickListener(new View.OnClickListener() {
                        @Override
                        public void onClick(View _view) {
                                    startActivityForResult(img3, REQ_CD_IMG3);
                        }
            });
            img_product4.setOnClickListener(new View.OnClickListener() {
                        @Override
                        public void onClick(View _view) {
                                    startActivityForResult(img4, REQ_CD_IMG4);
                        }
            });
            if (getIntent().getStringExtra("item").equals("Hotel")) {
                  location2.setVisibility(View.GONE);
            }
            else {
                  location1.setVisibility(View.GONE);
            }
      }
      
      @Override
      protected void onActivityResult(int _requestCode, int _resultCode, Intent _data) {
            super.onActivityResult(_requestCode, _resultCode, _data);
            
            switch (_requestCode) {
                  case REQ_CD_IMGMAIN:
                  if (_resultCode == Activity.RESULT_OK) {
                        ArrayList<String> _filePath = new ArrayList<>();
                        if (_data != null) {
                              if (_data.getClipData() != null) {
                                    for (int _index = 0; _index < _data.getClipData().getItemCount(); _index++) {
                                          ClipData.Item _item = _data.getClipData().getItemAt(_index);
                                          _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _item.getUri()));
                                    }
                              }
                              else {
                                    _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _data.getData()));
                              }
                        }
                        str_main_img = _filePath.get((int)(0));
                        product.setImageBitmap(FileUtil.decodeSampleBitmapFromPath(str_main_img, 1024, 1024));
                  }
                  else {
                        
                  }
                  break;
                  
                  case REQ_CD_IMG1:
                  if (_resultCode == Activity.RESULT_OK) {
                        ArrayList<String> _filePath = new ArrayList<>();
                        if (_data != null) {
                              if (_data.getClipData() != null) {
                                    for (int _index = 0; _index < _data.getClipData().getItemCount(); _index++) {
                                          ClipData.Item _item = _data.getClipData().getItemAt(_index);
                                          _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _item.getUri()));
                                    }
                              }
                              else {
                                    _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _data.getData()));
                              }
                        }
                        str_img1 = _filePath.get((int)(0));
                        imageview1.setImageBitmap(FileUtil.decodeSampleBitmapFromPath(str_img1, 1024, 1024));
                        img_product2.setVisibility(View.VISIBLE);
                  }
                  else {
                        
                  }
                  break;
                  
                  case REQ_CD_IMG2:
                  if (_resultCode == Activity.RESULT_OK) {
                        ArrayList<String> _filePath = new ArrayList<>();
                        if (_data != null) {
                              if (_data.getClipData() != null) {
                                    for (int _index = 0; _index < _data.getClipData().getItemCount(); _index++) {
                                          ClipData.Item _item = _data.getClipData().getItemAt(_index);
                                          _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _item.getUri()));
                                    }
                              }
                              else {
                                    _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _data.getData()));
                              }
                        }
                        str_img2 = _filePath.get((int)(0));
                        imageview2.setImageBitmap(FileUtil.decodeSampleBitmapFromPath(str_img2, 1024, 1024));
                        img_product3.setVisibility(View.VISIBLE);
                  }
                  else {
                        
                  }
                  break;
                  
                  case REQ_CD_IMG3:
                  if (_resultCode == Activity.RESULT_OK) {
                        ArrayList<String> _filePath = new ArrayList<>();
                        if (_data != null) {
                              if (_data.getClipData() != null) {
                                    for (int _index = 0; _index < _data.getClipData().getItemCount(); _index++) {
                                          ClipData.Item _item = _data.getClipData().getItemAt(_index);
                                          _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _item.getUri()));
                                    }
                              }
                              else {
                                    _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _data.getData()));
                              }
                        }
                        str_img3 = _filePath.get((int)(0));
                        imageview3.setImageBitmap(FileUtil.decodeSampleBitmapFromPath(str_img3, 1024, 1024));
                        img_product4.setVisibility(View.VISIBLE);
                  }
                  else {
                        
                  }
                  break;
                  
                  case REQ_CD_IMG4:
                  if (_resultCode == Activity.RESULT_OK) {
                        ArrayList<String> _filePath = new ArrayList<>();
                        if (_data != null) {
                              if (_data.getClipData() != null) {
                                    for (int _index = 0; _index < _data.getClipData().getItemCount(); _index++) {
                                          ClipData.Item _item = _data.getClipData().getItemAt(_index);
                                          _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _item.getUri()));
                                    }
                              }
                              else {
                                    _filePath.add(FileUtil.convertUriToFilePath(getApplicationContext(), _data.getData()));
                              }
                        }
                        str_img4 = _filePath.get((int)(0));
                        imageview4.setImageBitmap(FileUtil.decodeSampleBitmapFromPath(str_img4, 1024, 1024));
                  }
                  else {
                        
                  }
                  break;
                  default:
                  break;
            }
      }
      
      public void _changeActivityFont(final String _fontname) {
            fontName = "fonts/".concat(_fontname.concat(".ttf"));
            overrideFonts(this,getWindow().getDecorView());
      }
      private void overrideFonts(final android.content.Context context, final View v) {
            
            try {
                  Typeface
                  typeace = Typeface.createFromAsset(getAssets(), fontName);;
                  if ((v instanceof ViewGroup)) {
                        ViewGroup vg = (ViewGroup) v;
                        for (int i = 0;
                        i < vg.getChildCount();
                        i++) {
                              View child = vg.getChildAt(i);
                              overrideFonts(context, child);
                        }
                  }
                  else {
                        if ((v instanceof TextView)) {
                              ((TextView) v).setTypeface(typeace);
                        }
                        else {
                              if ((v instanceof EditText )) {
                                    ((EditText) v).setTypeface(typeace);
                              }
                              else {
                                    if ((v instanceof Button)) {
                                          ((Button) v).setTypeface(typeace);
                                    }
                              }
                        }
                  }
            }
            catch(Exception e)
            
            {
                  SketchwareUtil.showMessage(getApplicationContext(), "Error Loading Font");
            };
      }
      
      
      public void _Prog_Dialogue_show(final boolean _ifShow, final String _title, final String _message) {
            if (_ifShow) {
                  if (prog == null){
                        prog = new ProgressDialog(this);
                        prog.setMax(100);
                        prog.setIndeterminate(true);
                        prog.setCancelable(false);
                        prog.setCanceledOnTouchOutside(false);
                  }
                  prog.setMessage(_message);
                  prog.show();
            }
            else {
                  if (prog != null){
                        prog.dismiss();
                  }
            }
      }
      private ProgressDialog prog;
      {
      }
      
      
      public void _empty() {
            str_main_img_url = "";
            str_main_1_url = "";
            str_main_2_url = "";
            str_main_3_url = "";
            str_main_4_url = "";
            edittext3.setText("");
            edittextCall.setText("");
            edittextWA.setText("");
            edittext1.setText("");
            edittext2.setText("");
            edittext1.setText("");
            
            
            
            
            
      }
      
      
      @Deprecated
      public void showMessage(String _s) {
            Toast.makeText(getApplicationContext(), _s, Toast.LENGTH_SHORT).show();
      }
      
      @Deprecated
      public int getLocationX(View _v) {
            int _location[] = new int[2];
            _v.getLocationInWindow(_location);
            return _location[0];
      }
      
      @Deprecated
      public int getLocationY(View _v) {
            int _location[] = new int[2];
            _v.getLocationInWindow(_location);
            return _location[1];
      }
      
      @Deprecated
      public int getRandom(int _min, int _max) {
            Random random = new Random();
            return random.nextInt(_max - _min + 1) + _min;
      }
      
      @Deprecated
      public ArrayList<Double> getCheckedItemPositionsToArray(ListView _list) {
            ArrayList<Double> _result = new ArrayList<Double>();
            SparseBooleanArray _arr = _list.getCheckedItemPositions();
            for (int _iIdx = 0; _iIdx < _arr.size(); _iIdx++) {
                  if (_arr.valueAt(_iIdx))
                  _result.add((double)_arr.keyAt(_iIdx));
            }
            return _result;
      }
      
      @Deprecated
      public float getDip(int _input) {
            return TypedValue.applyDimension(TypedValue.COMPLEX_UNIT_DIP, _input, getResources().getDisplayMetrics());
      }
      
      @Deprecated
      public int getDisplayWidthPixels() {
            return getResources().getDisplayMetrics().widthPixels;
      }
      
      @Deprecated
      public int getDisplayHeightPixels() {
            return getResources().getDisplayMetrics().heightPixels;
      }
}
