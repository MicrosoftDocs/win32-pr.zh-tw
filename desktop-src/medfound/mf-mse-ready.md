---
description: 定義媒體來源延伸模組的不同就緒狀態。
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: MF_MSE_READY 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849524"
---
# <a name="mf_mse_ready-enumeration"></a>MF \_ MSE \_ 就緒列舉

定義媒體來源延伸模組的不同就緒狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ 就緒 \_ 已關閉**
</dt> <dd>

媒體來源已關閉。

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE 已 \_ 就緒 \_ 開啟**
</dt> <dd>

媒體來源已開啟。

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF \_ MSE \_ 就緒已 \_ 結束**
</dt> <dd>

媒體來源已結束。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎列舉](media-foundation-enumerations.md)
</dt> </dl>

 

 




