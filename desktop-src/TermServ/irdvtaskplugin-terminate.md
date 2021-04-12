---
title: IRDVTaskPlugin Terminate 方法
description: 在工作代理程式關閉時呼叫。
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Terminate 方法遠端桌面服務
- Terminate 方法遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，Terminate 方法
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384873"
---
# <a name="irdvtaskpluginterminate-method"></a>IRDVTaskPlugin：： Terminate 方法

在工作代理程式關閉時呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hr* \[在\]
</dt> <dd>

指出關機是否因為正常關機或失敗。 如果關機正常，則會包含 **\_ [確定]**。 否則，它會包含 **HRESULT** 錯誤碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

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

 

 





