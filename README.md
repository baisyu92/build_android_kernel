因為[KernelSU_Actions](https://github.com/xiaoleGun/KernelSU_Action)太多人用了，有可能發生和`MagiskOnWSA`一樣的問題，所以就自己搞了一個。話雖這麼說，但我根本不會這些，所以都是參考KernelSU_Actions寫出來的，內容就當作有87%一樣吧。

# 適用範圍(?
大多數GKI 2.0以下的應該都能用，不能用可能不是你的問題

# 說明
Fork這個倉庫，然後自己研究，應該不用10分鐘就要會用了。\
編譯完成後會打包成AnyKernel3，已關閉設備驗證，使用Recovery或刷寫工具刷入

# 選項說明
### **KernelSU URL**
Kernel(核心/內核)的倉庫網址

### **Branch**
倉庫要使用的分支名稱

### **Device defconfig**
設備的配置檔案名稱，有的要加`vendor/`，你應該有能力判斷

### **Boot format**
編譯出來的檔案格式，可以用`magiskboot`查詢，詳細請參考[此處](https://topjohnwu.github.io/Magisk/tools.html)

### **GCC version**
AOSP GCC應該有較高的相容性。Eva GCC版本較新，有些似乎要用這個才能成功

### **Clang version**
要使用的Clang版本，填`clang-`後面的字串。例如`clang-r487747/`，則填入`r487747`就好了。可用版本參考[這裡](https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+/refs/heads/master)，未來可能加入其他Google上游分支

### **Extra build commands**
編譯縮需要的額外指令，不輸入可能會編譯失敗，兩個指令中間需要空格

### **Add KernelSU**
加入[KernelSU](https://kernelsu.org/)，需要先將Kprobe的相關功能開啟，或手動修補後，才使用此選項。Stable為穩定版，Dev為開發版本，不打算支援手動指定版本

### **CROSS_COMPILE_ARM32**
有的需要加入此指令才能正常編譯
