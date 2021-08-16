---
title: 'IWMDRMNonSilentLicenseAquisition GetURL 方法 (Wmdrmsdk .h) '
description: GetURL 方法會抓取授權挑戰應張貼至其中的 URL。
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL 方法 windows Media 格式
- GetURL 方法 windows Media Format，IWMDRMNonSilentLicenseAquisition 介面
- IWMDRMNonSilentLicenseAquisition 介面 windows Media Format，GetURL 方法
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7979d82363b21b58563a606c31a99d069a60a3bc5b2da162a7339513c2867bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084705"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>IWMDRMNonSilentLicenseAquisition：： GetURL 方法

**GetURL** 方法會抓取授權挑戰應張貼至其中的 URL。

## <a name="syntax"></a>語法


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrURL* \[擴展\]
</dt> <dd>

接收 URL 之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMNonSilentLicenseAquisition 介面**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





