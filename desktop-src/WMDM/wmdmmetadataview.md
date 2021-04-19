---
title: WMDMMetadataView 結構
description: WMDMMetadataView 結構定義了元資料檢視。 內容是根據此定義來組織。
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- WMDMMetadataView 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985950"
---
# <a name="wmdmmetadataview-structure"></a>WMDMMetadataView 結構

**WMDMMetadataView** 結構定義了元資料檢視。 內容是根據此定義來組織。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>成員

<dl> <dt>

**pwszViewName**
</dt> <dd>

寬字元之以 null 結束的字串指標，其中包含視圖名稱。 這是用來做為顯示這個視圖之根節點的名稱。

</dd> <dt>

**nDepth**
</dt> <dd>

包含視圖深度的整數，表示用於視圖的嵌套元資料標記數目。

</dd> <dt>

**ppwszTags**
</dt> <dd>

嵌套標記的元資料標記字串陣列。

</dd> </dl>

## <a name="examples"></a>範例

下列程式碼會建立元資料檢視：


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



上述程式碼會組織內容，如下所示：

<dl> 我的觀點<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





