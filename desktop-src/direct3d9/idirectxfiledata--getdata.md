---
description: 抓取其中一個物件成員的資料，或所有成員的資料。 已取代。
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'IDirectXFileData：： DXFile 方法 (.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 428bff1f3fd76cd7c4589d5084435f8a675ab0d73bf0ff02052b2212d2c2dea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728964"
---
# <a name="idirectxfiledatagetdata-method"></a>IDirectXFileData：：：：的方法

抓取其中一個物件成員的資料，或所有成員的資料。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szMember* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要取得其資料之成員名稱的指標。 指定 **Null** 以抓取所有必要的成員資料。

</dd> <dt>

*pcbSize* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

接收 ppvData 緩衝區大小的指標（以位元組為單位）。

</dd> <dt>

*ppvData* \[擴展\]
</dt> <dd>

類型： **void \* \***

緩衝區指標的位址，用來接收與 szMember 相關聯的資料。 如果 szMember 為 **Null**，則 ppvData 會設定為指向在連續記憶體區塊中包含所有必要成員資料的緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADARRAYSIZE、DXFILEERR \_ BADDATAREFERENCE、DXFILEERR \_ BADVALUE。

## <a name="remarks"></a>備註

這個方法會抓取資料物件所需成員的資料，但不會取得選擇性 (子) 成員的資料。 使用 [**IDirectXFileData：： GetNextObject**](idirectxfiledata--getnextobject.md) 來取出子物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
