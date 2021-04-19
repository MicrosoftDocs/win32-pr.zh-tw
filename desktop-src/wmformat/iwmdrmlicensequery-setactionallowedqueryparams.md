---
title: 'IWMDRMLicenseQuery SetActionAllowedQueryParams 方法 (Wmdrmsdk .h) '
description: 使用 QueryActionAllowed 方法時，SetActionAllowedQueryParams 方法會設定環境特定的資訊，以取得更精確的查詢結果。
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- SetActionAllowedQueryParams 方法 windows Media 格式
- SetActionAllowedQueryParams 方法 windows Media Format，IWMDRMLicenseQuery 介面
- IWMDRMLicenseQuery 介面 windows Media Format，SetActionAllowedQueryParams 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987019"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>IWMDRMLicenseQuery：： SetActionAllowedQueryParams 方法

使用 [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)方法時， **SetActionAllowedQueryParams** 方法會設定環境特定的資訊，以取得更精確的查詢結果。

## <a name="syntax"></a>語法


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fIsMF* \[在\]
</dt> <dd>

指定是否使用 Microsoft 媒體基礎 SDK 的物件來呈現內容。 **FALSE** 表示由 Windows MEDIA 格式 SDK 的物件呈現。 這是選擇性參數。

</dd> <dt>

*dwAppSecLevel* \[在\]
</dt> <dd>

查詢應用程式的安全性層級。 只有在使用 Windows Media 格式 SDK 的物件時，此值才很重要，在此情況下， *fIsMF* 應該設為 **FALSE**。 這是選擇性參數。

</dd> <dt>

*fHasSerialNumber* \[在\]
</dt> <dd>

指定複製作業的目標裝置是否具有序號。 這個參數是選擇性的，只適用于複製作業的查詢。

</dd> <dt>

*bstrDeviceCert* \[在\]
</dt> <dd>

使用適用于可攜式裝置的 Windows Media DRM 時，目標裝置的裝置憑證。 這個參數是選擇性的，只適用于複製作業的查詢。

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

[**IWMDRMLicenseQuery 介面**](iwmdrmlicensequery.md)
</dt> <dt>

[**查詢詳細的許可權資訊**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





