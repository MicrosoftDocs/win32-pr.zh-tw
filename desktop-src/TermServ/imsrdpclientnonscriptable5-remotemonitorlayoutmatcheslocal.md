---
title: IMsRdpClientNonScriptable5 RemoteMonitorLayoutMatchesLocal 屬性
description: 指定遠端監視配置是否與本機監視器版面配置相同。
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- RemoteMonitorLayoutMatchesLocal 屬性遠端桌面服務
- RemoteMonitorLayoutMatchesLocal 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RemoteMonitorLayoutMatchesLocal 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235879a80e7e2a90207ee9b7852e73a26874c0961d7394fa80f2cf85e7452362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138721"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>IMsRdpClientNonScriptable5：： RemoteMonitorLayoutMatchesLocal 屬性

指定遠端監視配置是否與本機監視器版面配置相同。 如果此屬性包含 **VARIANT \_ TRUE**，則遠端監視配置與本機監視器版面配置相同。 如果此屬性包含 **變體 \_ FALSE**，則遠端和本機監視器會有不同的版面配置。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>屬性值

接收屬性值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





