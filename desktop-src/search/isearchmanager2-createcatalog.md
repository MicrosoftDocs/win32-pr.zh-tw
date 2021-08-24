---
description: 在 Windows Search 索引子中建立新的自訂目錄，並傳回它的參考。
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: ISearchManager2：： Start-createcatalog 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 34a4ceb37045ebbae62e04da0b5395673ed498c56189a26f2abaa376c960c511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597748"
---
# <a name="isearchmanager2createcatalog-method"></a>ISearchManager2：： Start-createcatalog 方法

在 Windows Search 索引子中建立新的自訂目錄，並傳回它的參考。

## <a name="syntax"></a>語法


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszCatalog* \[在\]
</dt> <dd>

類型： **[ **LPCWSTR**](../winprog/windows-data-types.md)**

要建立的目錄名稱。 可以是呼叫者所選取的任何名稱，必須只包含標準的英數位元和底線。

</dd> <dt>

*ppCatalogManager* \[擴展\]
</dt> <dd>

類型： **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

成功時，會以 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 介面指標的形式傳回所建立目錄的參考。 在呼叫的應用程式完成使用之後，必須在此介面上呼叫 Release () 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

HRESULT，指出作業的狀態：



| 傳回碼                                                                             | 描述                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 目錄先前未存在且已建立。 傳回的目錄參考。<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 目錄先前已存在，參考至所傳回的目錄。<br/>                       |



 

失敗的 HRESULT：無法建立目錄或傳遞的引數無效。

## <a name="remarks"></a>備註

呼叫以在 Windows Search 索引子中建立新的目錄。 建立之後，傳回的 [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 管理員上的方法可以用來新增要編制索引的位置、監視索引編制程式，以及建立要傳送至索引子的查詢並取得結果。 如需詳細資訊，請參閱「管理索引」檔： https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
