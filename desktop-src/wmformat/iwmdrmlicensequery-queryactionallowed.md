---
title: 'IWMDRMLicenseQuery QueryActionAllowed 方法 (Wmdrmsdk .h) '
description: QueryActionAllowed 方法會在本機授權存放區上執行查詢，以抓取適用于指定金鑰識別碼的一或多個 DRM 動作的授權狀態。
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- QueryActionAllowed 方法 windows Media 格式
- QueryActionAllowed 方法 windows Media Format，IWMDRMLicenseQuery 介面
- IWMDRMLicenseQuery 介面 windows Media Format，QueryActionAllowed 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989655"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>IWMDRMLicenseQuery：： QueryActionAllowed 方法

**QueryActionAllowed** 方法會在本機授權存放區上執行查詢，以抓取適用于指定金鑰識別碼的一或多個 DRM 動作的授權狀態。

## <a name="syntax"></a>語法


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKID* \[在\]
</dt> <dd>

要查詢的索引鍵識別碼。 只會評估適用于此金鑰識別碼的授權。

</dd> <dt>

*bstrMinReqIndivVersion* \[在\]
</dt> <dd>

在 ASF 檔案的標頭中指定的最小安全性版本。 這是選擇性參數。 傳遞 **Null** 以執行沒有此資訊的查詢。

</dd> <dt>

*cActionsToQuery* \[在\]
</dt> <dd>

要查詢的動作數目。 必須將此值設定為針對 *rgbstrActionsToQuery* 和 *rgdwQueryResult* 參數傳遞之陣列中的元素數目。

</dd> <dt>

*\[ rgbstrActionsToQuery \]*\[in\]
</dt> <dd>

要查詢的一或多個許可權的陣列。 此陣列必須包含 *cActionsToQuery* 所指定的元素數目。 每個元素都必須設定為下列其中一個常數：



| 常數                                         | 描述                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ActionAllowed \_ 播放             | 包含在查詢中播放內容的許可權。                              |
| g \_ wszWMDRM \_ ActionAllowed \_ Copy                 | 包含以查詢將內容複寫到外部裝置或媒體的許可權。 |
| g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn         | 包含在查詢中，將內容複寫到 CD 做為播放清單的一部分。  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | 包含以查詢從內容建立縮圖影像的許可權。     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | 包含在查詢中將內容複寫到 CD 的許可權。                        |



 

</dd> <dt>

*\[ rgdwQueryResult \]*\[out\]
</dt> <dd>

一或多個 DWORD 變數的陣列，這些變數會接收 *rgbstrActionsToQuery* 所指定許可權的查詢結果。 如果允許某項動作，則對應的元素會設定為零。 如果不允許某個動作，則會使用位 OR 運算，將專案設定為一或多個 [**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果**](drm-action-allowed-query-results.md) 列舉。 此陣列必須包含 *cActionsToQuery* 所指定的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

查詢播放和複製許可權時，您會先設定環境參數，以取得更精確的結果。 使用 [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) 方法來設定環境參數。 燒錄許可權的查詢結果不會受到環境參數的影響;您可以安全地使用預設值。

**QueryActionAllowed** 方法所傳回的結果是從本機授權存放區中的零或多個授權匯總而來。 如果遇到啟用的結果，此方法可能無法搜尋套用至金鑰識別碼的所有授權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseQuery 介面**](iwmdrmlicensequery.md)
</dt> <dt>

[**查詢簡單的許可權資訊**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





