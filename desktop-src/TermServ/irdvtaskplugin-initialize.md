---
title: IRDVTaskPlugin Initialize 方法
description: 呼叫以初始化工作代理程式。
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize 方法遠端桌面服務
- Initialize 方法遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，Initialize 方法
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14f4a002a0b33e403c02dba74385edd21e211fb27bcfb144c7a9ddc080a40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606101"
---
# <a name="irdvtaskplugininitialize-method"></a>IRDVTaskPlugin：： Initialize 方法

呼叫以初始化工作代理程式。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNotifySink* \[在\]
</dt> <dd>

類型： **[ **IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\***

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)介面的指標，工作代理程式會使用此介面與觸發程式代理程式進行通訊。 如果不再需要此介面，您必須釋放這個介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | Windows 7 Enterprise<br/>   |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





