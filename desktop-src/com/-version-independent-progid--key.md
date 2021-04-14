---
title: 與版本無關的 ProgID 金鑰
description: 將 ProgID 與 CLSID 產生關聯。 此索引鍵可用來判斷物件應用程式的最新版本。
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464104"
---
# <a name="version-independent-progid-key"></a>與版本無關的 ProgID 金鑰

將 ProgID 與 CLSID 產生關聯。 此索引鍵可用來判斷物件應用程式的最新版本。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>備註

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

<與 *版本無關的 ProgID*> 的格式 <*程式*>。 <*元件*>，以句號分隔，沒有空格，且沒有版本號碼。 與版本無關的 ProgID （例如 ProgID）可以註冊為人們可讀取的名稱。

*Progid* 是類別的最新已安裝版本的 progid。

應用程式必須在與 *版本無關的 ProgID* 金鑰下註冊與版本無關的程式設計識別碼。 與版本無關的 ProgID 指的是應用程式的類別，而且不會從版本變更為版本，而是在所有 versionsâ中的剩餘常數（例如 Microsoft Word 檔）。 它會與宏語言搭配使用，並參考目前安裝的應用程式類別版本。 與版本無關的 ProgID 必須對應至最新版本的物件應用程式名稱。

例如，當容器應用程式使用工具列按鈕建立圖表或資料表時，會使用與版本無關的 ProgID。 在這種情況下，應用程式可以使用與版本無關的 ProgID 來判斷所需物件應用程式的最新版本。

與版本無關的 ProgID 只會由應用程式程式碼儲存和維護。 當指定與版本無關的 ProgID 時， [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 函數會傳回目前版本的 CLSID。

您可以使用 [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 和 [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) ，在這兩種標記法之間進行轉換。

您可以使用 [**IOleObject：： GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) 或 [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) ，將識別碼變更為可顯示的字串。

如果未使用自訂處理常式，則專案應設定為 OLE32.DLL，如下列範例所示：

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<ProgID> 關鍵](-progid--key.md)
</dt> </dl>

 

 




