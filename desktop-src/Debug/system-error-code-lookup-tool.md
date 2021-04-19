---
description: 說明如何使用 Microsoft 錯誤查閱工具來尋找 Windows 中十六進位錯誤碼的文字說明。
title: Microsoft 錯誤查閱工具
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973767"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="7280a-103">Microsoft 錯誤查閱工具</span><span class="sxs-lookup"><span data-stu-id="7280a-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="7280a-104">Microsoft 錯誤查閱工具會顯示與十六進位狀態碼 (或其他程式碼) 相關聯的郵件內文。</span><span class="sxs-lookup"><span data-stu-id="7280a-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="7280a-105">這段文字是在各種 Microsoft 原始程式碼標頭檔中定義的，例如 Winerror.h .h、Setupapi.log .h 等等。</span><span class="sxs-lookup"><span data-stu-id="7280a-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="7280a-106">此工具是由 Microsoft 數位簽署。</span><span class="sxs-lookup"><span data-stu-id="7280a-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="7280a-107">以下是檔案下載的 SHA256 資訊：</span><span class="sxs-lookup"><span data-stu-id="7280a-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="7280a-108">演算法</span><span class="sxs-lookup"><span data-stu-id="7280a-108">Algorithm</span></span> |<span data-ttu-id="7280a-109">雜湊</span><span class="sxs-lookup"><span data-stu-id="7280a-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="7280a-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="7280a-110">SHA256</span></span> |<span data-ttu-id="7280a-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span><span class="sxs-lookup"><span data-stu-id="7280a-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="7280a-112">商務環境可能會限制可執行檔檔案，以及從何處執行的檔案。</span><span class="sxs-lookup"><span data-stu-id="7280a-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="7280a-113">在您下載並執行此工具之前，請檢查下列詳細資料：</span><span class="sxs-lookup"><span data-stu-id="7280a-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="7280a-114">您是否必須有許可權或安全性例外，才能下載或執行此工具？</span><span class="sxs-lookup"><span data-stu-id="7280a-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="7280a-115">您是否可以在電腦上儲存及執行此工具 (例如，在 [檔] 資料夾中) ？</span><span class="sxs-lookup"><span data-stu-id="7280a-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="7280a-116">或者，您必須在特製化的電腦（例如中央檔案伺服器）上儲存及執行此工具嗎？</span><span class="sxs-lookup"><span data-stu-id="7280a-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="7280a-117">使用方式</span><span class="sxs-lookup"><span data-stu-id="7280a-117">Usage</span></span>

1. <span data-ttu-id="7280a-118">選取 [此連結](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)以下載工具。</span><span class="sxs-lookup"><span data-stu-id="7280a-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="7280a-119">如果您未在步驟1中指定位置，請移至您的下載資料夾，然後將下載的檔案 (Err_6.4.5.exe) 複製或移動到您將在其中儲存工具的資料夾。</span><span class="sxs-lookup"><span data-stu-id="7280a-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="7280a-120">您不需要擴充或安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="7280a-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="7280a-121">如果您將檔案複製或移動到作業系統 **Path** 環境變數中所列的資料夾，它就會在任何命令提示字元中運作。</span><span class="sxs-lookup"><span data-stu-id="7280a-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="7280a-122">開啟命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="7280a-122">Open a Command Prompt window.</span></span> <span data-ttu-id="7280a-123">如有必要，請將目錄變更為錯誤查閱工具的位置。</span><span class="sxs-lookup"><span data-stu-id="7280a-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="7280a-124">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="7280a-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="7280a-125">在此命令中， \<*error code*> 代表您要查閱的十六進位程式碼。</span><span class="sxs-lookup"><span data-stu-id="7280a-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="7280a-126">範例</span><span class="sxs-lookup"><span data-stu-id="7280a-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="7280a-127">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7280a-127">More information</span></span>

<span data-ttu-id="7280a-128">請記住，這是「時間點」工具。</span><span class="sxs-lookup"><span data-stu-id="7280a-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="7280a-129">Microsoft Error Lookup 工具會將大部分的 Microsoft 錯誤碼解碼為工具的編譯日期。</span><span class="sxs-lookup"><span data-stu-id="7280a-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="7280a-130">當新的 Windows 版本加入新的事件和錯誤碼時，您可能必須下載新版本的錯誤查閱工具。</span><span class="sxs-lookup"><span data-stu-id="7280a-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="7280a-131">請檢查 Microsoft 下載中心以取得新版本，或查看 [錯誤碼](system-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="7280a-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
