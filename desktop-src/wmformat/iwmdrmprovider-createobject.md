---
title: 'IWMDRMProvider CreateObject 方法 (Wmdrmsdk .h) '
description: CreateObject 方法會抓取指定介面的指標，並視需要建立執行物件。
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- CreateObject 方法 windows Media 格式
- CreateObject 方法 windows Media Format，IWMDRMProvider 介面
- IWMDRMProvider 介面 windows Media Format，CreateObject 方法
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983982"
---
# <a name="iwmdrmprovidercreateobject-method"></a>IWMDRMProvider：： CreateObject 方法

**CreateObject** 方法會抓取指定介面的指標，並視需要建立執行物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* \[在\]
</dt> <dd>

要建立之介面的識別碼。 設定為下列其中一個值。

-   IID \_ IWMDRMLicenseManagement
-   IID \_ IWMDRMLicenseQuery
-   IID \_ IWMDRMNetReceiver
-   IID \_ IWMDRMNetTransmitter
-   IID \_ IWMDRMSecurity

</dd> <dt>

*ppvObject* \[擴展\]
</dt> <dd>

接收所要求介面位址之指標的位址。

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

[**IWMDRMProvider 介面**](iwmdrmprovider.md)
</dt> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**IWMDRMLicenseQuery 介面**](iwmdrmlicensequery.md)
</dt> <dt>

[**IWMDRMNetReceiver 介面**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetTransmitter 介面**](iwmdrmnettransmitter.md)
</dt> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> </dl>

 

 





