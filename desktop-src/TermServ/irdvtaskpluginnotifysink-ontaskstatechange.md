---
title: IRDVTaskPluginNotifySink OnTaskStateChange 方法
description: 用來通知觸發程式代理程式工作的狀態已變更。
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- OnTaskStateChange 方法遠端桌面服務
- OnTaskStateChange 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，OnTaskStateChange 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998029"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>IRDVTaskPluginNotifySink：： OnTaskStateChange 方法

用來通知觸發程式代理程式工作的狀態已變更。

## <a name="syntax"></a>語法


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrIdentifier* \[在\]
</dt> <dd>

類型： **BSTR**

工作的識別碼。 這是傳遞給 [**StartTask**](irdvtaskplugin-starttask.md) 方法的識別碼。

</dd> <dt>

*狀態* \[在\]
</dt> <dd>

類型： **[ **RDV \_ 工作 \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

[**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)列舉值，這個值會指定工作的新狀態。

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

[**RDV \_ 工作 \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





