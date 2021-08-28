---
title: IWMDRMDevice SetMeterResponse 方法
description: SetMeterResponse 方法會設定計量回應。
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- SetMeterResponse 方法 windows Media 裝置管理員
- SetMeterResponse 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，SetMeterResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b05941619d30ea067dc594e05b7b427ec5d825ef3e0c3c441cdfb3c723e94d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619568"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>IWMDRMDevice：： SetMeterResponse 方法

**SetMeterResponse** 方法會設定計量回應。

## <a name="syntax"></a>語法


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbMeterResponse* \[在\]
</dt> <dd>

要設定的計量回應。

</dd> <dt>

*cbMeterResponse* \[在\]
</dt> <dd>

計量回應的大小（以位元組為單位）。

</dd> <dt>

*pdwFlags* \[擴展\]
</dt> <dd>

回應旗標。 此值必須是下列其中一個旗標。



| 旗標                            | 描述              |
|---------------------------------|--------------------------|
| WMDRM \_ 計量 \_ 回應 \_ 全部     | 所有計量回應。     |
| WMDRM \_ 計量 \_ 回應 \_ 部分 | 部分計量回應。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





