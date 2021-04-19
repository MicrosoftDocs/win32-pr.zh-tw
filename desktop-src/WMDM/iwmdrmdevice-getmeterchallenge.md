---
title: IWMDRMDevice GetMeterChallenge 方法
description: GetMeterChallenge 方法會捕獲計量挑戰。
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- GetMeterChallenge 方法 windows Media 裝置管理員
- GetMeterChallenge 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetMeterChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979890"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>IWMDRMDevice：： GetMeterChallenge 方法

**GetMeterChallenge** 方法會捕獲計量挑戰。

## <a name="syntax"></a>語法


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrMeterCert* \[在\]
</dt> <dd>

內容擁有者傳送給主機電腦以收集裝置上相關計量資料的計量憑證

</dd> <dt>

*ppbMeterChallenge* \[擴展\]
</dt> <dd>

已取出計量挑戰結果。

</dd> <dt>

*pcbMeterChallenge* \[擴展\]
</dt> <dd>

計量挑戰的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

計量資料會收集並儲存在裝置上的 DRM 資料存放區中，以啟用計量的內容。 將會記錄播放等動作。 呼叫此函式時，裝置會以 XML 檔的形式收集 DRM 資料存放區中的計量資料，並將其傳送至 hostcomputer。 如果有太多資料，則會分階段傳送。

當主機電腦收到計量資料時，它會透過網際網路將資料傳送到計量憑證中指定的 URL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





