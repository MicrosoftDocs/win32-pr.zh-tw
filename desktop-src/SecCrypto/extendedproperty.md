---
description: 表示 Microsoft 擴充的屬性。
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998861"
---
# <a name="extendedproperty-object"></a>ExtendedProperty 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**ExtendedProperty** 物件代表 Microsoft 擴充的屬性。

## <a name="when-to-use"></a>使用時機

**ExtendedProperty** 物件是用來執行下列工作：

-   設定或取出擴充屬性的類型。
-   設定或取出用來編碼擴充屬性的編碼類型。

## <a name="members"></a>成員

**ExtendedProperty** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ExtendedProperty** 物件具有這些屬性。



| 屬性                                             | 存取類型           | Description                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | 讀取/寫入<br/> | 可設定或抓取擴充屬性之類型的 [**CAPICOM \_ PROPID**](capicom-propid.md) 列舉值。<br/> 這是預設屬性。<br/> |
| [**值**](extendedproperty-value.md)<br/>   | 讀取/寫入<br/> | 可設定或抓取擴充屬性資料之 [**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md) 列舉的值。<br/>                              |



 

## <a name="remarks"></a>備註

**ExtendedProperty** 物件是由 [**ExtendedProperties**](extendedproperties.md)集合所使用。

您可以建立 **ExtendedProperty** 物件，而且不安全地編寫腳本。 **ExtendedProperty** 物件的 PROGID 是 CAPICOM。ExtendedProperty。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
