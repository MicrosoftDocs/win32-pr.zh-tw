---
title: 使用參考 Dll 從 .NET 使用 BITS
description: 下列範例示範如何從 .NET 程式呼叫 BITS COM 介面
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679255"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>使用參考 Dll 從 .NET 和 c # 呼叫 BITS

從 .NET 程式呼叫 BITS COM 類別的其中一種方式，就是使用[MIDL](/windows/desktop/Midl/using-the-midl-compiler-2)和[tlbimp.exe](/dotnet/framework/tools/tlbimp-exe-type-library-importer)工具，從 Windows SDK 中的位[IDL](/windows/desktop/Midl/midl-start-page) (介面定義語言) 檔案建立參考 DLL 檔案。 參考 DLL 是 BITS COM 類別的一組類別包裝函式;然後，您可以直接從 .NET 使用包裝函式類別。

使用自動建立之參考 Dll 的替代方法是使用來自 [GitHub](https://github.com/) 和 [NuGet](https://www.nuget.org/)的協力廠商 .net 位包裝函式。 這些包裝函式通常有更自然的 .NET 程式設計樣式，但它們可能會落後 BITS 介面中的變更和更新。

## <a name="creating-the-reference-dlls"></a>建立參考 Dll
### <a name="bits-idl-files"></a>BITS IDL 檔案

您將從一組 BITS IDL 檔案開始。 這些是完整定義 BITS COM 介面的檔案。 這些檔案位於 **Windows 套件** 目錄中，並命名為 bits *版本*.idl (例如，bits10_2 .idl) 除了版本1.0 檔案，也就是僅限 bits .idl。 建立新版本的 BITS 時，也會建立新的 BITS IDL 檔案。

您也可能想要修改一份 SDK 位 IDL 檔案，以使用未自動轉換成 .NET 對等專案的 BITS 功能。 稍後會討論可能的 IDL 檔案變更。

BITS IDL 檔案包含其他數個以傳址方式提供的 IDL 檔案。 它們也會進行嵌套，因此，如果您使用一個版本，則會包含所有較低的版本。

針對您想要在程式中作為目標的每個位版本，您將需要該版本的一個參考 DLL。 例如，如果您想要撰寫可在 BITS 1.5 和更新版本上運作的程式，但在 BITS 10.2 存在時有其他功能，您需要轉換 bits1_5 .idl 和 bits10_2 .idl 檔。


### <a name="midl-and-tlbimp-utilities"></a>MIDL 和 TLBIMP 公用程式

[MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft 介面定義語言) 公用程式會將描述 BITS COM 介面的 IDL 檔案，轉換成 TLB (型別程式庫) 檔。 MIDL 工具相依于 CL 公用程式 (C 預處理器) ，以正確地讀取 IDL 語言檔案。 CL 公用程式是 Visual Studio 的一部分，當您在 Visual Studio 安裝中包含 C/c + + 功能時，會安裝此公用程式。

MIDL 公用程式通常會建立一組 C 和 H (C 語言程式碼和 C 語言標頭) 檔案。 您可以藉由將輸出傳送至 NUL：裝置來隱藏這些額外的檔案。 例如，設定/dlldata NUL： switch 將會隱藏 dlldata.c .c 檔案的建立。 下列範例命令會顯示哪些參數應設定為 NUL：。

[Tlbimp.exe](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (型別程式庫匯入工具) 公用程式會讀取 TLB 檔案，並建立對應的參考 DLL 檔案。 


### <a name="example-commands-for-midl-and-tlbimp"></a>MIDL 和 TLBIMP 的命令範例

這是用來產生一組參考檔案的完整命令集範例。 您可能需要根據您的 Visual Studio 和 Windows SDK 安裝來修改命令，並根據您目標的 BITS 功能和作業系統版本。 

此範例會建立一個目錄來放置參考 DLL 檔案，並建立環境變數 BITSTEMP 來指向該目錄。 

然後，範例命令會執行 Visual Studio 安裝程式所建立的 vsdevcmd.bat 檔案。 這個 .BAT 檔案會設定您的路徑和一些環境變數，以便執行 MIDL 和 TLBIMP.EXE 命令。 它也會設定 WindowsSdkDir 和 WindowsSDKLibVersion 變數，以指向最新的 Windows SDK 目錄。

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
執行這些命令之後，您會在 BITSTEMP 目錄中有一組參照 Dll。

### <a name="adding-the-reference-dlls-to-your-project"></a>將參考 Dll 新增至專案

若要在 c # 專案中使用參考 DLL，請在 Visual Studio 中開啟您的 c # 專案。 在 [方案總管中，以滑鼠右鍵按一下 [參考]，然後按一下 [加入參考]。 然後按一下 [流覽] 按鈕，然後按一下 [新增] 按鈕。 流覽至含有參考 Dll 的目錄，選取它們，然後按一下 [新增]。 在 [參考管理員] 視窗中，將會檢查參照 Dll。 然後按一下 [確定]。

BITS 參考 Dll 現在已加入至您的專案。

參考 DLL 檔案中的資訊將內嵌至您的最終程式。 您不需要與您的程式一起寄送參照 DLL 檔案。您只需要寄送。Exe。 

您可以變更參考 Dll 是否內嵌至最終 EXE。 您可以使用 [ [內嵌 Interop 類型](/dotnet/framework/interop/how-to-add-references-to-type-libraries) ] 屬性來設定是否將內嵌參考 dll。 這可以根據每個參考來完成。 預設值為 True，以內嵌 Dll。

## <a name="modifying-idl-files-for-more-complete-net-code"></a>修改 IDL 檔案以取得更完整的 .NET 程式碼

 (Microsoft 介面定義語言) 檔案的 BITS IDL 可原封不動地使用，以建立 BackgroundCopyManager DLL 檔案。 但是，所產生的 .NET 參考 DLL 將會遺漏某些產生無法翻譯聯集，而且某些結構和列舉會有難以使用的名稱。 本節將說明一些您可以進行的變更，讓 .NET DLL 更完整且更容易使用。

### <a name="simpler-enum-names"></a>更簡單的列舉名稱

BITS IDL 檔案通常會定義如下的列舉值：
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
BG_AUTH_TARGET 是 typedef 的名稱;實際的列舉未命名。 這通常不會造成 C 程式碼發生問題，但無法順利轉譯以搭配 .NET 程式使用。 系統會自動建立新的名稱，但它可能看起來像 _MIDL___MIDL_itf_bits4_0_0005_0001_0001 而不是人類看得懂的值。 您可以藉由更新 MIDL 檔案以包含列舉名稱來修正此問題。

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

允許列舉名稱與 typedef 名稱相同。 某些程式設計人員有一個命名慣例，其中 (例如，藉由在列舉名稱之前加上底線，將底線放在) ，但這只會混淆 .NET 翻譯。 

### <a name="string-types-in-unions"></a>等位中的字串類型

BITS IDL 檔案會使用 LPWSTR (long 指標來傳遞字串) 慣例的寬字元字串。 雖然這在傳遞函式參數時很有用 (例如 GetDisplayName ( [out] LPWSTR * pVal) 方法) ，但是當字串是等位的一部分時，就無法運作。 例如，bits5_0 .idl 檔包含 BITS_FILE_PROPERTY_VALUE 聯集：

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

LPWSTR 欄位將不會包含在 .NET 版本的聯集內。 若要修正此問題，請將 LPWSTR 變更為 WCHAR *。 產生的欄位 (呼叫的字串) 將會以 IntPtr 的形式傳遞。 使用 System.runtime.interopservices.outattribute. PtrToStringAuto (值將此轉換成字串。字串) ;方法。

### <a name="unions-in-structures"></a>結構中的等位

有時內嵌在結構中的聯集不會包含在結構中。 例如，在 Bits1_5 .idl 中，BG_AUTH_CREDENTIALS 的定義如下：
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

BG_AUTH_CREDENTIALS_UNION 定義為聯集，如下所示：
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
BG_AUTH_CREDENTIALS 中的 [認證] 欄位將不會包含在 .NET 類別定義中。

請注意，不論 BG_AUTH_SCHEME，union 都會定義為一律是 BG_BASIC_CREDENTIALS。 因為等位不會當做聯集使用，所以我們可以直接傳遞 BG_BASIC_CREDENTIALS，如下所示：
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>使用 C 的位#

### <a name="recommended-using-statement"></a>建議使用語句

在 c # 中設定某些 using 語句，會減少您需要輸入以使用不同位版本的字元數。 名稱 "BITSReference" 來自參考 DLL 的名稱。

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>快速範例：下載檔案

以下提供簡單但完整的 c # 程式碼程式碼片段，以從 URL 下載檔案。 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

在此範例程式碼中，會建立名為 mgr 的 BITS 管理員。 它會直接對應至 [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) 介面。 

從管理員建立新的作業。 作業是 >batchclient.joboperations.createjob 方法上的 out 參數。 傳入的也是不需要是唯一) 的作業 (名稱，以及下載類型，也就是下載作業。 工作識別碼的位 GUID 也會填入。

一旦建立作業之後，您就可以使用 AddFile 方法，將新的下載檔案新增至作業。 您必須傳入兩個字串，一個用於遠端檔案 (URL 或檔案共用) ，另一個用於本機檔案。 

新增檔案之後，請在作業上呼叫 Resume 來啟動它。 然後，程式碼會等到工作處於最終狀態 (錯誤或傳輸) ，然後才會完成。

### <a name="bits-versions-casting-and-queryinterface"></a>BITS 版本、轉換和 QueryInterface

您會發現，您通常必須在程式中使用舊版的 BITS 物件和較新的版本。  

例如，當您建立工作物件時，即使您要使用較新的管理員物件，且有較新的 IBackgroundCopyJob 物件可用，還是會收到 IBackgroundCopyJob (部分的 BITS 1.0 版) 。 因為 >batchclient.joboperations.createjob 方法不接受最新版本的介面，所以您無法直接建立較新版本。

使用 .NET cast 從較舊的型別物件轉換成較新的型別物件。 轉換會自動依適當情況呼叫 COM QueryInterface。 

在此範例中，有一個名為 "job" 的位 IBackgroundCopyJob 物件，而我們想要將它轉換成名為 "job5" 的 IBackgroundCopyJob5 物件，以便我們可以呼叫 BITS 5.0 GetProperty 方法。 我們只是轉換成 IBackgroundCopyJob5 型別，如下所示：

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

Job5 變數將使用正確的 QueryInterface，由 .NET 初始化。 

如果您的程式碼可能在不支援特定版本 BITS 的系統上執行，您可以嘗試轉換並攔截 InvalidCastException。 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

常見的問題是當您嘗試轉換成錯誤的物件類型時。 .NET 系統不知道 BITS 介面之間的真正關聯性。 如果您要求的是錯誤類型的介面，.NET 將會嘗試為您進行處理，並會因為 InvalidCastException 和 HResult 0x80004002 (E_NOINTERFACE) 而失敗。

### <a name="working-with-bits-versions-10_1-and-10_2"></a>使用 BITS 版本10_1 和10_2

在某些版本的 Windows 10 上，您無法使用10.1 或10.2 介面直接建立 BITS IBackgroundCopyManager 物件。 相反地，您必須使用多個版本的 BackgroundCopyManager DLL 參考檔案。 例如，您可以使用1.5 版本建立 IBackgroundCopyManager 物件，然後使用10.1 或10.2 版本來轉換產生的作業或檔案物件。

