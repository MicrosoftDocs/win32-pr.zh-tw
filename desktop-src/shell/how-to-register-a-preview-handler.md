---
description: 本主題說明如何註冊與指定資料類型相關聯的預覽處理常式。
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: 如何註冊預覽處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e1879261750609015acee2ccea1bc6f48f82df78ac7c18cbb2f46fa493c4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223437"
---
# <a name="how-to-register-a-preview-handler"></a>如何註冊預覽處理常式

本主題說明如何註冊與指定資料類型相關聯的預覽處理常式。 為了方便說明，本主題中的範例會使用 .xyz 檔案類型。 註冊預覽處理常式是標準的檔案關聯型註冊。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

首先，副檔名與 ProgID 相關聯。 下列專案會將 **xyzfile** ProgID 子機碼與 .xyz 副檔名產生關聯。

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

**Xyzfile** ProgID 子機碼會與其他 progid 儲存，如下所示：

```
HKEY_CLASSES_ROOT
   xyzfile
```

每個預覽處理常式 ProgID 子機碼都包含名為 **shellex** 的子機碼，其中包含 *名為* **{8895b1c6-b41f-4c1c-a562-0d564250836f}** 的子機 該子機碼的存在會告訴系統處理常式是預覽處理常式。

**{8895b1c6-b41f-4c1c-a562-0d564250836f}** 子機碼的預設值是處理常式 (CLSID) 的類別識別碼。 **Xyzfile** ProgID 子機碼的範例如下所示，關聯 CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154} 的處理常式。

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a>步驟 2:

接下來，在預覽處理常式的 [ **CLSID** ] 下新增子機碼。 範例如下所示。 以下是個別專案的說明。

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

子機碼的預設值 (在此處， **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) 並非必要或使用。 但是，將其設定為未當地語系化的字串可協助您偵測註冊問題。

DisplayName 專案中 .dll 資源的負號 (-101) 存在於舊版的原因。 相反地，圖示專案不需要減號。

AppID 值會提供與副檔名相關聯之應用程式的 appid 參考， (儲存在 **HKEY \_ 類別 \_ 根目錄** \\ **AppID** 下。 此處所使用的值（{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}）是 Prevhost.exe 代理主機的識別碼。 32位預覽處理常式在64位作業系統上安裝時，應使用 **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C}。

**InprocServer32** 子機碼底下的專案包含對副檔名之 ProgID 子機碼的參考，以及 [VersionIndependentProgID](../com/versionindependentprogid.md)的專案。

### <a name="step-3"></a>步驟 3：

最後，預覽處理常式必須加入至所有預覽處理常式的清單中。 這份清單是由系統用來為顯示目的列舉所有已註冊預覽處理常式的優化。 同樣地，預設值並非必要，它只會輔助偵錯工具。

> [!Note]  
> 在 Windows 7 中，如果已為電腦的所有使用者安裝應用程式，請使用 HKEY \_ 本機 \_ 電腦; 如果只針對一位使用者，請使用 HKEY \_ 目前的 \_ 使用者。

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預覽處理常式和 Shell 預覽主機](preview-handlers.md)
</dt> <dt>

[建立預覽處理常式](building-preview-handlers.md)
</dt> <dt>

[預覽處理常式指導方針](preview-handler-guidelines.md)
</dt> </dl>

 

 
