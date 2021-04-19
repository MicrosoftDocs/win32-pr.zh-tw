---
title: 'IWMDRMLicenseQuery QueryLicenseState 方法 (Wmdrmsdk .h) '
description: QueryLicenseState 方法會查詢本機授權存放區，以取得適用于一或多個特定許可權之金鑰識別碼的授權資訊。
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- QueryLicenseState 方法 windows Media 格式
- QueryLicenseState 方法 windows Media Format，IWMDRMLicenseQuery 介面
- IWMDRMLicenseQuery 介面 windows Media Format，QueryLicenseState 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977629"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>IWMDRMLicenseQuery：： QueryLicenseState 方法

**QueryLicenseState** 方法會查詢本機授權存放區，以取得適用于一或多個特定許可權之金鑰識別碼的授權資訊。

## <a name="syntax"></a>語法


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKID* \[在\]
</dt> <dd>

要查詢的索引鍵識別碼。 只會評估適用于此金鑰識別碼的授權。

</dd> <dt>

*cActionsToQuery* \[在\]
</dt> <dd>

要查詢的動作數目。 必須將此值設定為針對 *rgbstrActionsToQuery* 和 *rgResultStateData* 參數傳遞之陣列中的元素數目。

</dd> <dt>

*\[ rgbstrActionsToQuery \]*\[in\]
</dt> <dd>

要查詢的一或多個許可權的陣列。 此陣列必須包含 *cActionsToQuery* 所指定的元素數目。 每個元素都必須設定為下列其中一個常數。



| 常數                                        | 描述                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ LicenseState \_ 備份               | 包含以查詢有關備份和還原授權之許可權的詳細資料。                                                               |
| g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | 包含，以查詢與使用者群組共用內容的許可權詳細資料，作為共同作業播放案例的一部分。          |
| g \_ wszWMDRM \_ LicenseState \_ Copy                 | 包含以查詢將內容複寫到外部裝置或媒體的許可權詳細資料。                                                 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | [包含] 以查詢將內容複寫到 CD 的右邊詳細資料。                                                                        |
| g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | 包含，以查詢將內容複寫到不支援 (SDMI) 之安全數位媒體計畫之裝置的許可權詳細資料。 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | 包含以查詢有關將內容複寫到支援 SDMI 之裝置的許可權詳細資料。                                           |
| g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage | 包含以查詢從內容建立縮圖影像右邊的詳細資料。                                                     |
| g \_ wszWMDRM \_ LicenseState \_ 播放             | 包含以查詢有關播放內容之右邊的詳細資料。                                                                              |
| g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | 包含，以查詢將內容複寫到 CD 做為播放清單一部分的右邊詳細資料。                                                  |



 

</dd> <dt>

*\[ rgResultStateData \]*\[out\]
</dt> <dd>

一或多個 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md) 結構的陣列，此結構會接收適用于 *rgbstrActionsToQuery* 參數的對應元素右側的授權狀態資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

將會搜尋並評估套用至指定金鑰識別碼的所有授權。 結果會進行匯總，因此每個 **DRM \_ 授權 \_ 狀態 \_ 資料** 結構可能包含來自多個授權的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseQuery 介面**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





