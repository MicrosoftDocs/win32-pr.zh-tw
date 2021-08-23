---
title: IMsRdpPreferredRedirectionInfo UseRedirectionServerName 屬性
description: 取得和設定是否使用重新導向伺服器名稱。
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- UseRedirectionServerName 屬性遠端桌面服務
- UseRedirectionServerName 屬性遠端桌面服務，IMsRdpPreferredRedirectionInfo 介面
- IMsRdpPreferredRedirectionInfo 介面遠端桌面服務，UseRedirectionServerName 屬性
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1bb57bacafbc3061cee6cb49b09a8fdbf8187026a378deff605b90472ed6394
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513248"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a>IMsRdpPreferredRedirectionInfo：： UseRedirectionServerName 屬性

取得和設定是否使用重新導向伺服器名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a>屬性值

是否要使用重新導向伺服器名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                    |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo 定義為 FDD029F9-9574-4DEF-8529-64B521CCCAA4<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





