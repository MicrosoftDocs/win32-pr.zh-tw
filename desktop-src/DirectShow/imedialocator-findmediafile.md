---
description: FindMediaFile 方法會搜尋檔案，如果成功，則會抓取檔案的路徑。
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'IMediaLocator：： FindMediaFile 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc1acda4a3bc6e2d93ae8b7024ef34f759c11c5c4d487a09d3be3a3542e0c445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818935"
---
# <a name="imedialocatorfindmediafile-method"></a>IMediaLocator：： FindMediaFile 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會搜尋檔案，如果成功，則會抓取檔案 `FindMediaFile` 的路徑。

## <a name="syntax"></a>語法


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*輸入* 
</dt> <dd>

檔案名，包括路徑，也就是最後已知的檔案所在的路徑。 若為時間軸中的來源物件，請使用目前的媒體名稱。

</dd> <dt>

*FilterString* 
</dt> <dd>

包含篩選字串配對的 **BSTR** ，格式為 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFilter** 成員所需。 如果媒體定位器顯示 [開啟檔案] 對話方塊，則會使用此篩選器。 如果 Flags 參數未包含 SFN VALIDATEF 快顯旗 *標*，則此值可以是 **Null** \_ \_ 。

</dd> <dt>

*pOutput* 
</dt> <dd>

如果變數與 *輸入* 中包含的值不同，而且方法成功找到檔案，則為收到檔案實際路徑的變數指標。

</dd> <dt>

*旗標* 
</dt> <dd>

零或多個旗標的位元組合。 如需可能旗標的清單，請參閱 [**檔案名驗證旗標**](file-name-validation-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

[開啟檔案] 對話方塊的篩選字串（由 *FilterString* 參數指定）包含內部 Null 字元。 例如，影片 \\ 0 \*.avi\\ 0 \\ 0 是有效的篩選字串。 您無法使用 **SysAllocStr** 函式來配置 BSTR，因為該函式需要以 null 終止的字串，且會在第一個 Null 字元截斷字串。 因此，請使用類似 **SysAllocStringLen** 的函式，其中包含長度的明確參數：


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



如果使用者取消 [開啟檔案] 對話方塊，方法會傳回 E \_ FAIL。

方法會為 *pOutput* 中的 **BSTR** 配置記憶體。 應用程式必須呼叫 **SysFreeString** 來釋放記憶體。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaLocator 介面**](imedialocator.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 
