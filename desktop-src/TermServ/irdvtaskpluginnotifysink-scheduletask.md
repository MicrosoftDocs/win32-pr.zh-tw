---
title: IRDVTaskPluginNotifySink ScheduleTask 方法
description: 由工作代理程式呼叫以排程工作。
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask 方法遠端桌面服務
- ScheduleTask 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，ScheduleTask 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844279"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>IRDVTaskPluginNotifySink：： ScheduleTask 方法

由工作代理程式呼叫以排程工作。

## <a name="syntax"></a>語法


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ftStartTime* \[在\]
</dt> <dd>

類型： **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

最早的工作開始時間（UTC）。

</dd> <dt>

*ftEndTime* \[在\]
</dt> <dd>

類型： **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

工作結束時間（UTC）。 如果未指定任何結束時間，則將 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 集合傳遞至全部零。

</dd> <dt>

*ftDeadline* \[在\]
</dt> <dd>

類型： **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

工作期限（UTC 格式）。 這是用來設定其開始視窗內多個工作的優先順序。 如果應啟動多項工作，則會先啟動具有最早期限的工作。

</dd> <dt>

*bstrLabel* \[在\]
</dt> <dd>

類型： **BSTR**

工作的標籤。 這會傳遞至 [**StartTask**](irdvtaskplugin-starttask.md) 方法。

</dd> <dt>

*bstrIdentifier* \[在\]
</dt> <dd>

類型： **BSTR**

工作的識別碼。 這會傳遞至 [**StartTask**](irdvtaskplugin-starttask.md) 方法。

</dd> <dt>

*saCoNtext* \[在\]
</dt> <dd>

類型： **SAFEARRAY (BYTE)**

工作的選擇性資料。 這會傳遞至 [**StartTask**](irdvtaskplugin-starttask.md) 方法。

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

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

