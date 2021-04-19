---
description: 指定是否在網路來源中啟用 Real-Time 串流通訊協定 (RTSP) 傳輸。
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: 'MFNETSOURCE_ENABLE_RTSP 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac191e6e244a8e341fef0dccd274293f09846aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974092"
---
# <a name="mfnetsource_enable_rtsp-property"></a>MFNETSOURCE \_ ENABLE \_ RTSP 屬性

指定是否在網路來源中啟用 Real-Time 串流通訊協定 (RTSP) 傳輸。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

布林 (**LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ ENABLE \_ RTSP** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[支援的通訊協定](supported-protocols.md)
</dt> </dl>

 

 




