---
description: 當受保護的存放區顯示使用者介面時，定義其提示行為。
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: 'PST_PROMPTINFO 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b127ae7156c97f1fad41dd99cb575228ac9934dfb75c2e3765f3de1fa38e0a93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386208"
---
# <a name="pst_promptinfo-structure"></a>PST \_ PROMPTINFO 結構

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

當受保護的存放區顯示使用者介面時，定義其提示行為。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

此結構的大小。

</dd> <dt>

**dwPromptFlags**
</dt> <dd>

會忽略此旗標。



| 值                                                                                                                                                                                                                                          | 意義                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**PST \_PF \_ 一律 \_ 顯示**</dt> <dt>0x00000001</dt> </dl> | 要求提供者顯示提示對話方塊給使用者，即使此存取不需要。 <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**PST \_PF \_ 絕不會 \_ 顯示**</dt> <dt>0x00000002</dt> </dl>    | 不要向使用者顯示提示對話方塊。<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

使用者介面的父視窗控制碼。 **HwndApp** 成員會決定使用者介面的出現位置。 如果傳遞 **Null** ，則會將桌面視為父視窗。

</dd> <dt>

**szPrompt**
</dt> <dd>

提示字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**ReadItem**](ipstore-readitem.md)
</dt> <dt>

[**WriteItem**](ipstore-writeitem.md)
</dt> </dl>

 

 
