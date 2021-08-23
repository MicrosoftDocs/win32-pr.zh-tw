---
description: 指定 proxy 伺服器的主機名稱。
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: 'MFNETSOURCE_PROXYHOSTNAME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82746763c937bdca388782cb0882b536c0b9e93b660e0f8e0a04426e5b48a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663668"
---
# <a name="mfnetsource_proxyhostname-property"></a>MFNETSOURCE \_ PROXYHOSTNAME 屬性

指定 proxy 伺服器的主機名稱。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

寬字元字串 (**WCHAR** \*) 

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PROXYHOSTNAME** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

當建立 proxy 定位器物件時，應用程式可以使用這個屬性來設定預設 proxy 定位器。 若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。 當 proxy 定位器設定成以手動模式操作時，應用程式必須設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[網路來源的 Proxy 支援](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




