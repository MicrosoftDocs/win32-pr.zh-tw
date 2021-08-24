---
description: 提供 COM 標準方法來管理受保護的儲存資料項目。
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: 'IPStore 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d6404d182a0c46de222b64892caa8b0e853610c980bfb79d286f781277493cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749704"
---
# <a name="ipstore-interface"></a>IPStore 介面

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

\[此介面可能會在未來的 Windows 版本中變更或無法使用。\]

提供 COM 標準方法來管理受保護的儲存資料項目。 [**PStoreCreateInstance**](pstorecreateinstance.md)方法會傳回這個介面的指標。

## <a name="members"></a>成員

**IPStore** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IPStore** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IPStore** 介面具有這些方法。



| 方法                                                   | 描述                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | 從受保護的儲存體關閉指定的資料項目。<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | 在指定的型別內建立指定的子類型。<br/>                                                   |
| [**CreateType**](ipstore-createtype.md)                 | 使用指定的名稱建立指定的型別。<br/>                                                        |
| [**DeleteItem**](ipstore-deleteitem.md)                 | 從受保護的儲存體中刪除指定的專案。<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | 從受保護的儲存體中刪除指定的專案子類型。<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | 從受保護的儲存體中刪除指定的類型。<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | 傳回用來列舉受保護儲存資料庫中專案的子類型介面指標。<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | 傳回介面，以列舉受保護資料庫中目前註冊之類型的子類型。<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | 傳回介面，以列舉受保護資料庫中目前註冊的類型。<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | 抓取儲存提供者的相關資訊。<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | 未實作。<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | 捕獲與子類型相關聯的資訊。<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | 抓取與類型相關聯的資訊。<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | 開啟多個存取的專案。<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | 未實作。<br/>                                                                                           |
| [**ReadItem**](ipstore-readitem.md)                     | 從受保護的儲存體讀取指定的資料項目。<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | 設定指定的參數資訊。<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | 未實作。<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | 將資料項目寫入受保護的儲存體。<br/>                                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
