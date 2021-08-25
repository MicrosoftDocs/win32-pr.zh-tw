---
title: IMsTscAxEvents OnRequestContainerMinimize 方法
description: 當使用者在全螢幕模式下的連接列上按下最小化按鈕時呼叫。 引發此事件是容器應用程式本身最小化的要求。
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- OnRequestContainerMinimize 方法遠端桌面服務
- OnRequestContainerMinimize 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRequestContainerMinimize 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344bd85d8d224a5901517c55c8e0a95c854ed246e74a9d0c8def1eebae515305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125058"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>IMsTscAxEvents：： OnRequestContainerMinimize 方法

當使用者在全螢幕模式下的連接列上按下 **最小化** 按鈕時呼叫。 引發此事件是容器應用程式本身最小化的要求。

## <a name="syntax"></a>語法


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

只有在已啟用容器處理的全螢幕模式時，才會呼叫這個方法。如需詳細資訊，請參閱 [**IMsTscAdvancedSettings：:p 的 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





