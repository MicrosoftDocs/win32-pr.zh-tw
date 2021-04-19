---
title: 'IWMDRMLicense GetAnalogVideoRestrictionLevels 方法 (Wmdrmsdk .h) '
description: GetAnalogVideoRestrictionLevels 方法會抓取目前授權所設定的所有類比影片限制。
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- GetAnalogVideoRestrictionLevels 方法 windows Media 格式
- GetAnalogVideoRestrictionLevels 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetAnalogVideoRestrictionLevels 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989619"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>IWMDRMLicense：： GetAnalogVideoRestrictionLevels 方法

**GetAnalogVideoRestrictionLevels** 方法會抓取目前授權所設定的所有類比影片限制。

## <a name="syntax"></a>語法


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*\[ rgAnalogVideoRestrictions \]*\[out\]
</dt> <dd>

接收 [**WMDRM \_ 類比 \_ 影片 \_ 限制**](wmdrm-analog-video-restrictions.md) 結構的陣列。 設定為 **Null** ，以取得 *pcResctrictions* 中陣列的元素數目。

</dd> <dt>

*pcRestrictions* \[in、out\]
</dt> <dd>

限制陣列中的元素數目。 如果 *rgAnalogVideoRestrictions* 設定為 **Null**，則此值會設定為數組中所需的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

您必須為限制陣列配置記憶體。 若要這樣做，請先呼叫方法，並將 *rgAnalogVideoRestrictions* 設定為 **Null**，這會將 *pcRestrictions* 的值設定為所需的元素數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





