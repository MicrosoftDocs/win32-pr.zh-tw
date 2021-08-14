---
description: 列舉目錄定義檔之 CatalogFiles 區段中的成員檔案屬性 (CDF) 。
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: f1bffd01865b524b0f06003a6a46b8f81542d7f6113f98db55202e08d8dd7ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768893"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>CryptCATCDFEnumAttributesWithCDFTag 函式

\[**CryptCATCDFEnumAttributesWithCDFTag** 函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

**CryptCATCDFEnumAttributesWithCDFTag** 函式會列舉目錄定義檔之 **CatalogFiles** 區段中的成員檔案屬性 (CDF) 。 [MakeCat](makecat.md)會呼叫 **CryptCATCDFEnumAttributesWithCDFTag** 。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCDF* \[在\]
</dt> <dd>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)結構的指標。

</dd> <dt>

*pwszMemberTag* \[在\]
</dt> <dd>

識別類別目錄檔案成員之以 **null** 結束的字串指標。

</dd> <dt>

*pMember* \[在\]
</dt> <dd>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)結構的指標，其中包含成員資訊。

</dd> <dt>

*pPrevAttr* \[在\]
</dt> <dd>

*PCDF* 所指向之 CDF 中檔案成員屬性的 [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)結構指標。

</dd> <dt>

*pfnParseError* \[在\]
</dt> <dd>

使用者定義函數的指標，用來處理檔案剖析錯誤。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，此函式會傳回 [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) 結構的指標。 如果 **CryptCATCDFEnumAttributesWithCDFTag** 函式失敗，則會傳回 **Null** 指標。

## <a name="remarks"></a>備註

您通常會在迴圈中呼叫此函式，以列舉 CDF 中的所有類別目錄檔案成員屬性。 進入迴圈之前，請將 *pPrevAttr* 設定為 **Null**。 函數會傳回第一個屬性的指標。 針對迴圈的後續反覆運算，將 *pPrevAttr* 設定為函式的傳回值。

## <a name="examples"></a>範例

下列範例顯示 *pPrevAttr* 參數 () 的正確指派順序 `pAttr` 。


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
