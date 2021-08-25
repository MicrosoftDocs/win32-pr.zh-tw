---
title: IWMDRMLicense GetOutputProtectionLevels 方法
description: GetOutputProtectionLevels 方法會抓取指派給授權 (OPLs) 所有輸出保護層級的相關資訊。
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- GetOutputProtectionLevels 方法 windows Media 格式
- GetOutputProtectionLevels 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetOutputProtectionLevels 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771318"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>IWMDRMLicense：： GetOutputProtectionLevels 方法

**GetOutputProtectionLevels** 方法會抓取指派給授權 (OPLs) 所有輸出保護層級的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOPLs* \[擴展\]
</dt> <dd>

接收 OPL 資訊之 [**WMDRM \_ 輸出 \_ 保護 \_ 層級**](wmdrm-output-protection-levels.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





