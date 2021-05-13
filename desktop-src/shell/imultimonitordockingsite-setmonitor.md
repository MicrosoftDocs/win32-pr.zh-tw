---
description: 變更用於多個監視器系統上停駐工具列的監視器。
title: IMultiMonitorDockingSite：： SetMonitor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841939"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>IMultiMonitorDockingSite：： SetMonitor 方法

變更用於多個監視器系統上停駐工具列的監視器。

## <a name="syntax"></a>語法


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*punkSrc* \[在\]
</dt> <dd>

類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

物件的指標，該物件會執行正在更改監視的 [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) 介面。

</dd> <dt>

*hMonNew* \[在\]
</dt> <dd>

類型： **HMONITOR**

此監視器的控制碼，會取代現有的預設監視器。

</dd> <dt>

*phMonOld* \[擴展\]
</dt> <dd>

類型： **HMONITOR \***

當此函式傳回時，會包含先前預設監視器控制碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                   |



 

 
