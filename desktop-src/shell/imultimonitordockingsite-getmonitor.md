---
description: 取得目前的預設監視器。
title: IMultiMonitorDockingSite：： GetMonitor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991695"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>IMultiMonitorDockingSite：： GetMonitor 方法

取得目前的預設監視器。

## <a name="syntax"></a>語法


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*punkSrc* \[在\]
</dt> <dd>

類型： **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

物件的指標，該物件會執行正在要求監視的 [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)介面。

</dd> <dt>

*phMon* \[擴展\]
</dt> <dd>

類型： **HMONITOR \** _

當函式傳回時，會包含指向預設監視器控制碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                   |



 

 
