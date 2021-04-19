---
title: 'IWMDRMLicenseManagement DeleteLicense 方法 (Wmdrmsdk .h) '
description: DeleteLicense 方法會移除暫時本機授權存放區中的授權。
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- DeleteLicense 方法 windows Media 格式
- DeleteLicense 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，DeleteLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981639"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement：:D eleteLicense 方法

**DeleteLicense** 方法會移除暫時本機授權存放區中的授權。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKID* \[在\]
</dt> <dd>

金鑰識別碼 (要刪除的授權小孩) 。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

授權刪除選項旗標。 設定為下表中的其中一個值。



| 值                                    | 描述                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_立即刪除 WMDRM 的 \_ 授權 \_      | 指定應立即從存放區移除授權。                                                                                                                              |
| \_清除的 WMDRM 刪除 \_ 授權 \_ 標記 \_ \_ | 指定應標示為要刪除的授權，但在呼叫 [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) 方法之前，不應該從存放區中移除。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                            | Description                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 此方法已成功。<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | 指定的授權不存在於存放區中。<br/> -或-<br/> 找不到存放區。<br/> |



 

## <a name="remarks"></a>備註

若要從永久本機授權存放區刪除授權，您必須使用授權撤銷。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





