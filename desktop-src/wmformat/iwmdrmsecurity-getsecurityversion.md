---
title: 'IWMDRMSecurity GetSecurityVersion 方法 (Wmdrmsdk .h) '
description: GetSecurityVersion 方法會在用戶端電腦上抓取 DRM 子系統的版本。
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- GetSecurityVersion 方法 windows Media 格式
- GetSecurityVersion 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetSecurityVersion 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984034"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a>IWMDRMSecurity：： GetSecurityVersion 方法

**GetSecurityVersion** 方法會在用戶端電腦上抓取 DRM 子系統的版本。

## <a name="syntax"></a>語法


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrVersion* \[擴展\]
</dt> <dd>

接收 DRM 子系統版本號碼之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

版本號碼會以字串表示，由四個以句點分隔的數位所組成。 第一個數位是主要版本號碼，通常是設定為2。 第二個數字是次要版本號碼，範圍介於2到10之間。 第三個數字一律設定為0。 第四個數字設定為0或1，且為布林值，指出子系統是否已個別化。 例如，"2.4.0.1" 的版本號碼表示第二個主要版本的個別第四個次要版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> </dl>

 

 





