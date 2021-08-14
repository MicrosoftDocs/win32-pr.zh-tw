---
description: 描述如何使用 Microsoft 錯誤查閱工具，在 Windows 中尋找十六進位錯誤碼的文字說明。
title: Microsoft 錯誤查閱工具
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: 534b2af92b8dc0e906bd033e8ce1f0fbd08ead0cda21406d1818a318356db613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405888"
---
# <a name="the-microsoft-error-lookup-tool"></a>Microsoft 錯誤查閱工具

Microsoft 錯誤查閱工具會顯示與十六進位狀態碼 (或其他程式碼) 相關聯的郵件內文。 這段文字是在各種 Microsoft 原始程式碼標頭檔中定義的，例如 Winerror.h .h、Setupapi.log .h 等等。

此工具是由 Microsoft 數位簽署。 以下是檔案下載的 SHA256 資訊：  

|演算法 |雜湊 |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> 商務環境可能會限制可執行檔檔案，以及從何處執行的檔案。 在您下載並執行此工具之前，請檢查下列詳細資料：
> - 您是否必須有許可權或安全性例外，才能下載或執行此工具？
> - 您是否可以在電腦上儲存及執行此工具 (例如，在 [檔] 資料夾中) ？ 或者，您必須在特製化的電腦（例如中央檔案伺服器）上儲存及執行此工具嗎？

## <a name="usage"></a>使用方式

1. 選取 [此連結](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)以下載工具。
1. 如果您未在步驟1中指定位置，請移至您的下載資料夾，然後將下載的檔案 (Err_6.4.5.exe) 複製或移動到您將在其中儲存工具的資料夾。 您不需要擴充或安裝檔案。
   > [!NOTE]
   > 如果您將檔案複製或移動到作業系統 **Path** 環境變數中所列的資料夾，它就會在任何命令提示字元中運作。

1. 開啟命令提示字元視窗。 如有必要，請將目錄變更為錯誤查閱工具的位置。
1. 執行下列命令：
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > 在此命令中， \<*error code*> 代表您要查閱的十六進位程式碼。

## <a name="examples"></a>範例

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

## <a name="more-information"></a>更多資訊

請記住，這是「時間點」工具。 Microsoft Error Lookup 工具會將大部分的 Microsoft 錯誤碼解碼為工具的編譯日期。 當新版本的 Windows 加入新的事件和錯誤碼時，您可能必須下載新版本的錯誤查閱工具。 請檢查 Microsoft 下載中心以取得新版本，或查看 [錯誤碼](system-error-codes.md)。
