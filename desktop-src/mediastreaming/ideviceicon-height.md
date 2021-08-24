---
title: IDeviceIcon Height 方法
description: 抓取圖示的高度（以圖元為單位）。
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- Height 方法媒體串流 API
- Height 方法媒體串流 API，IDeviceIcon 介面
- IDeviceIcon 介面媒體串流 API，高度方法
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d813c572b0fc9e562d40326d830c5ef3530857601811df78c3acd541314b402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060288"
---
# <a name="ideviceiconheight-method"></a>IDeviceIcon：： Height 方法

抓取圖示的高度（以圖元為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收圖示高度的指標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

