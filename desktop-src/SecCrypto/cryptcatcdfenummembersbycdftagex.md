---
description: 列舉目錄定義檔之 CatalogFiles 區段中的個別檔案成員 (CDF) 。
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511173"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>CryptCATCDFEnumMembersByCDFTagEx 函式

\[**CryptCATCDFEnumMembersByCDFTagEx** 函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

**CryptCATCDFEnumMembersByCDFTagEx** 函式會列舉目錄定義檔之 **CatalogFiles** 區段中的個別檔案成員， (CDF) 。 [MakeCat](makecat.md)會呼叫 **CryptCATCDFEnumMembersByCDFTagEx** 。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCDF* \[在\]
</dt> <dd>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)結構的指標。

</dd> <dt>

*pwszPrevCDFTag* \[in、out\]
</dt> <dd>

識別類別目錄檔案成員之以 **null** 結束的字串指標。

</dd> <dt>

*pfnParseError* \[在\]
</dt> <dd>

使用者定義函數的指標，用來處理檔案剖析錯誤。

</dd> <dt>

*ppMember* \[在\]
</dt> <dd>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)結構的指標，其中包含檔案成員資訊。

</dd> <dt>

*fContinueOnError* \[在\]
</dt> <dd>

值，指定是否要在記憶體中保留最後一個列舉成員的參考。

</dd> <dt>

*pvReserved* \[在\]
</dt> <dd>

此參數為 reserved;請勿使用它。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，此函式會傳回以 **null** 結束的字串指標，以識別 CDF **CatalogFiles** 區段中的檔案成員。 如果 **CryptCATCDFEnumMembersByCDFTagEx** 函式失敗，則會傳回 **Null** 指標。

## <a name="remarks"></a>備註

您通常會在迴圈中呼叫此函式，以列舉 CDF 中的所有類別目錄檔案成員。 進入迴圈之前，請將 *pwszPrevCDFTag* 設定為 **Null**。 函數會傳回第一個成員的指標。 針對迴圈的後續反覆運算，將 *pwszPrevCDFTag* 設定為函式的傳回值。

## <a name="examples"></a>範例

下列範例顯示 *pwszPrevCDFTag* 參數 () 的正確指派順序 `pwszMemberTag` 。


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
