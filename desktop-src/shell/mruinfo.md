---
description: 包含定義最近使用的新 (MRU) 清單的資訊。 由 CreateMRUListW 使用。
title: MRUINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840759"
---
# <a name="mruinfo-structure"></a>MRUINFO 結構

包含定義最近使用的新 (MRU) 清單的資訊。 由 [**CreateMRUListW**](createmrulist.md)使用。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

結構的大小。

</dd> <dt>

**uMax**
</dt> <dd>

類型： **UINT**

</dd> <dd>

MRU 清單中專案的最大數目。

</dd> <dt>

**fFlags**
</dt> <dd>

類型： **UINT**

</dd> <dd>

下列一或多個旗標。

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_二元** (0x0001) 


</dt> <dd>

資料會以二進位資料的形式儲存在登錄中，而不是以字串資料的形式儲存。

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_CACHEWRITE** (0x0002) 


</dt> <dd>

只有在新增專案或從記憶體釋放 MRU 清單的資源時，才會將變更寫入儲存在登錄中的 MRU 版本。 請注意，在記憶體中，作用中的 MRU 版本會立即更新以回應任何內容變更或排序。

</dd> </dl> </dd> <dt>

**hKey**
</dt> <dd>

類型： **HKEY**

</dd> <dd>

目前開啟之索引鍵的控制碼，或下列其中一個預先定義的值，用來儲存 MRU 資料。

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**HKEY \_ 目前的 \_ 使用者**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ 本機 \_ 電腦**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

類型： **LPCTSTR**

</dd> <dd>

用來儲存 MRU 資料的子機碼。

</dd> <dt>

**lpfnCompare**
</dt> <dd>

類型： **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

選擇性資料比較函式的指標，可用來判斷專案是否存在於 MRU 清單中。 當使用 **mru \_ 二進位** 旗標建立 mru 清單時，這非常有用。 如果這個成員是 **Null**，則會使用標準字串比較函數;若為二進位資料，則會使用直接記憶體比較。

</dd> </dl>

## <a name="remarks"></a>備註

標頭檔中未定義此結構。 您必須自行定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |
| Unicode 與 ANSI 名稱<br/>   | **MRUINFOW** (Unicode) 和 **MRUINFOA** (ANSI) <br/>  |



 

 




