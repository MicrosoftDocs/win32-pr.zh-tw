---
description: Get 方法會抓取屬性集 GUID 和屬性識別碼所識別的屬性。
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'IKsPropertySet：： Get 方法 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: fbfd44002270209c055b5a4003d9062a6821aeffb3ce71de7977fc20d0c64e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652240"
---
# <a name="ikspropertysetget-method"></a>IKsPropertySet：： Get 方法

**Get** 方法會抓取屬性集 GUID 和屬性識別碼所識別的屬性。

## <a name="syntax"></a>語法


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*guidPropSet* \[在\]
</dt> <dd>

屬性集的 GUID。

</dd> <dt>

*dwPropID* \[在\]
</dt> <dd>

屬性集內屬性的識別碼。

</dd> <dt>

*pInstanceData* \[在\]
</dt> <dd>

位元組陣列的指標，其中包含屬性的實例資料。

</dd> <dt>

*cbInstanceData* \[在\]
</dt> <dd>

*PInstanceData* 中指定的陣列大小（以位元組為單位）。

</dd> <dt>

*pPropData* \[擴展\]
</dt> <dd>

接收屬性資料之位元組陣列的指標。

</dd> <dt>

*cbPropData* \[在\]
</dt> <dd>

*PPropData* 中指定的陣列大小（以位元組為單位）。

</dd> <dt>

*pcbReturned* \[擴展\]
</dt> <dd>

接收方法複製到 *pPropData* 陣列的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                              | 描述                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 成功。<br/>                                                         |
| <dl> <dt>**E \_ \_ 設定 \_ 不支援的設定**</dt> </dl> | 不支援屬性集。<br/>                               |
| <dl> <dt>**E \_ \_ \_ 不支援的識別碼**</dt> </dl>  | 指定的屬性集不支援屬性識別碼。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個名稱的另一個介面存在於 dsound .h 標頭檔中。 這兩個介面不相容。 [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol)介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。

 

若要抓取屬性，請配置此方法將填入的緩衝區。 若要判斷所需的緩衝區大小，請針對 *pPropData* 指定 **Null** ，並為 *cbPropData* 指定零 (0) 。 這個方法會在 *pcbReturned* 中傳回所需的緩衝區大小。

您必須在 Ksproxy 之前包含 Ks。

## <a name="examples"></a>範例

下列範例會藉由取出 **AMPROPERTY \_ 釘選 \_ 類別目錄** 屬性，查詢其釘選類別的 pin。  (參閱 [釘選屬性集](pin-property-set.md)。 ) 


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ksproxy。h</dt> </dl>    |
| 程式庫<br/>                  | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet 介面**](ikspropertyset.md)
</dt> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 
