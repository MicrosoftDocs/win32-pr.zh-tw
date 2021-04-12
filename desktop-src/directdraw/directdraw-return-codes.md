---
title: 'DirectDraw 傳回碼 (Ddraw) '
description: 錯誤會以負數值表示，而且無法合併。
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70ff2003edc382bac2823235f01f58ffea0d91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854039"
---
# <a name="directdraw-return-codes"></a>DirectDraw 傳回碼

錯誤會以負數值表示，而且無法合併。 下表列出 [DirectDraw 介面](directdraw-interfaces.md) 和 [directdraw 函數](directdraw-functions.md)的所有方法都可以傳回的值。 如需每個方法或函式可以傳回的錯誤碼清單，請參閱方法或函數描述。

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ 確定**
</dt> <dd> <dl> <dt>



要求已順利完成。


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ ALREADYINITIALIZED**
</dt> <dd> <dl> <dt>



物件已初始化。


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**
</dt> <dd> <dl> <dt>



DirectDrawClipper 物件會附加至已傳遞至 [**IDirectDrawSurface7：： BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) 方法呼叫的來源介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**
</dt> <dd> <dl> <dt>



介面無法附加至另一個要求的介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**
</dt> <dd> <dl> <dt>



介面無法與另一個要求的介面卸離。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**
</dt> <dd> <dl> <dt>



Windows 無法 (Dc) 建立任何更多裝置內容，或如果在此情況下，DC 已要求使用調色板索引介面，且顯示模式未建立調色板索引 (在此情況下，DirectDraw 無法在 DC) 中選取適當的調色板。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**
</dt> <dd> <dl> <dt>



無法複製主要和3D 表面，或隱含建立的表面。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**
</dt> <dd> <dl> <dt>



因為嘗試鎖定主要表面但沒有顯示控制項介面 (DCI) 支援，所以拒絕存取這個介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**
</dt> <dd> <dl> <dt>



嘗試對介面進行頁面鎖定失敗。 頁面鎖定無法在顯示記憶體介面或模擬的主要表面上運作。


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**
</dt> <dd> <dl> <dt>



嘗試對介面進行頁面解除鎖定失敗。 頁面解除鎖定無法在顯示記憶體介面或模擬的主要表面上運作。


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**
</dt> <dd> <dl> <dt>



嘗試為已監看視窗控制碼的 DirectDrawClipper 物件設定剪輯清單。


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**
</dt> <dd> <dl> <dt>



未指定此作業的來源色彩索引鍵。


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**
</dt> <dd> <dl> <dt>



目前不提供任何支援。


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**
</dt> <dd> <dl> <dt>



DirectX 7.0 的新新。 介面需要 DDSCAPS \_ 複雜旗標。


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**
</dt> <dd> <dl> <dt>



已針對此介面傳回 (DC) 的裝置內容。 只能針對每個介面抓取一個 DC。


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNTOWNSURFACE**
</dt> <dd> <dl> <dt>



另一個 directdraw 裝置無法直接使用一個 DirectDraw 裝置所建立的表面。


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**
</dt> <dd> <dl> <dt>



已經為此程式建立了表示此驅動程式的 DirectDraw 物件。


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR \_ 例外狀況**
</dt> <dd> <dl> <dt>



執行要求的作業時，發生例外狀況。


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**
</dt> <dd> <dl> <dt>



嘗試在已將合作層級設定為獨佔層級時進行設定。


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR 已 \_ 過期**
</dt> <dd> <dl> <dt>



資料已過期，因此不再有效。


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ 泛型**
</dt> <dd> <dl> <dt>



有未定義的錯誤條件。


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**
</dt> <dd> <dl> <dt>



提供之矩形的高度不是所需對齊的倍數。


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWNDALREADYSET**
</dt> <dd> <dl> <dt>



已設定 DirectDraw 合作等級的視窗控制碼。 當程式已建立表面或調色板時無法重設。


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**
</dt> <dd> <dl> <dt>



因為已將 DirectDraw 合作層級視窗控制碼子類別化，所以無法還原 DirectDraw 的狀態。


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**
</dt> <dd> <dl> <dt>



因為介面是隱含建立的介面，所以無法還原。


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**
</dt> <dd> <dl> <dt>



主要表面建立要求不符合現有的主要介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR \_ INVALIDCAPS**
</dt> <dd> <dl> <dt>



傳遞給回呼函式的一或多個功能位不正確。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**
</dt> <dd> <dl> <dt>



DirectDraw 不支援提供的剪輯清單。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**
</dt> <dd> <dl> <dt>



傳遞給 [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) 函數的全域唯一識別碼 (GUID) 不是有效的 DirectDraw 驅動程式識別碼。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INVALIDMODE**
</dt> <dd> <dl> <dt>



DirectDraw 不支援要求的模式。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INVALIDOBJECT**
</dt> <dd> <dl> <dt>



DirectDraw 收到的指標是不正確 DirectDraw 物件。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**
</dt> <dd> <dl> <dt>



傳遞給方法的一或多個參數不正確。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**
</dt> <dd> <dl> <dt>



像素格式的指定無效。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**
</dt> <dd> <dl> <dt>



目的地上重迭的位置已不再有效。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**
</dt> <dd> <dl> <dt>



提供的矩形無效。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**
</dt> <dd> <dl> <dt>



指定的資料流程包含不正確資料。


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**
</dt> <dd> <dl> <dt>



介面的類型錯誤。


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**
</dt> <dd> <dl> <dt>



一或多個介面已鎖定，導致要求的作業失敗。


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**
</dt> <dd> <dl> <dt>



有更多資料可供使用，而不是指定的緩衝區大小可保留。


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NEWMODE.OBJ**
</dt> <dd> <dl> <dt>



DirectX 7.0 的新新。 使用 DDSMT ISTESTREQUIRED 旗標呼叫 [**IDirectDraw7：： StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) 時 \_ ，它可能會傳回這個值，以表示部分或全部的解決方法都可以測試。 [**IDirectDraw7：： EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) 會傳回這個值，以表示測試已切換至新的顯示模式。


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**
</dt> <dd> <dl> <dt>



不存在立體硬體或模擬。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**
</dt> <dd> <dl> <dt>



沒有任何 Alpha 加速硬體存在或無法使用，導致要求的作業失敗。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**
</dt> <dd> <dl> <dt>



沒有任何位區傳輸硬體存在。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOCLIPLIST**
</dt> <dd> <dl> <dt>



沒有任何可用的剪輯清單。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**
</dt> <dd> <dl> <dt>



沒有任何 DirectDrawClipper 物件附加至介面物件。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**
</dt> <dd> <dl> <dt>



沒有任何色彩轉換硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**
</dt> <dd> <dl> <dt>



介面目前沒有色彩索引鍵。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**
</dt> <dd> <dl> <dt>



目的地色彩機碼沒有硬體支援。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**
</dt> <dd> <dl> <dt>



未使用 [**IDirectDraw7：： SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) 方法呼叫 create 函數。


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**
</dt> <dd> <dl> <dt>



尚未為此介面建立任何裝置內容 (DC) 。


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**
</dt> <dd> <dl> <dt>



沒有 DirectDraw 的 (ROP) 硬體可用的硬體。


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**
</dt> <dd> <dl> <dt>



不可能建立僅限硬體的 DirectDraw 物件建立;驅動程式不支援任何硬體。


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**
</dt> <dd> <dl> <dt>



無法使用目前的顯示驅動程式來支援 DirectDraw。


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**
</dt> <dd> <dl> <dt>



DirectX 7.0 的新新。 無法繼續進行測試，因為顯示配接器驅動程式並未列舉重新整理頻率。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOEMULATION**
</dt> <dd> <dl> <dt>



無法使用軟體模擬。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOEXCLUSIVEMODE**
</dt> <dd> <dl> <dt>



作業需要應用程式具有獨佔模式，但應用程式沒有獨佔模式。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**
</dt> <dd> <dl> <dt>



不支援翻轉可見的表面。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**
</dt> <dd> <dl> <dt>



嘗試在不先設定焦點視窗的情況下，建立或設定裝置視窗。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**
</dt> <dd> <dl> <dt>



沒有 GDI 存在。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOHWND**
</dt> <dd> <dl> <dt>



Clipper 通知需要視窗控制碼，或先前未將任何視窗控制碼設定為合作層級視窗控制碼。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**
</dt> <dd> <dl> <dt>



沒有具有 mipmap 功能的材質對應硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**
</dt> <dd> <dl> <dt>



沒有任何鏡像硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**
</dt> <dd> <dl> <dt>



DirectX 7.0 的新新。 因為監視器沒有相關聯的 EDID 資料，所以無法繼續測試。


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**
</dt> <dd> <dl> <dt>



嘗試從不支援非本機視訊記憶體的裝置配置非本機視頻記憶體。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**
</dt> <dd> <dl> <dt>



裝置不支援優化表面。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**
</dt> <dd> <dl> <dt>



[**IDirectDrawSurface7：： GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition)方法是在未呼叫 [**IDirectDrawSurface7：： UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay)方法的覆迭上呼叫，以建立為目的地。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**
</dt> <dd> <dl> <dt>



沒有任何重迭硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**
</dt> <dd> <dl> <dt>



沒有任何調色板物件附加到這個介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**
</dt> <dd> <dl> <dt>



16或256色調色板沒有硬體支援。


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**
</dt> <dd> <dl> <dt>



沒有適當的點陣操作硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**
</dt> <dd> <dl> <dt>



沒有任何旋轉硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**
</dt> <dd> <dl> <dt>



沒有任何身歷聲硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**
</dt> <dd> <dl> <dt>



沒有硬體支援可延展。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**
</dt> <dd> <dl> <dt>



目前沒有支援立體表面的硬體。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



DirectDrawSurface 物件不是使用4位色調色板，而要求的作業需要4位色調色板。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



DirectDrawSurface 物件未使用4位色彩索引選擇區，而要求的作業需要4位的色彩索引選擇區。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



DirectDrawSurface 物件不是使用8位色調色板，且要求的作業需要8位色板。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**
</dt> <dd> <dl> <dt>



針對 nonoverlay 介面呼叫覆迭元件。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**
</dt> <dd> <dl> <dt>



無法執行操作，因為沒有任何材質對應硬體存在或無法使用。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR \_ NOTFLIPPABLE**
</dt> <dd> <dl> <dt>



嘗試翻轉無法翻轉的介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR \_ NOTFOUND**
</dt> <dd> <dl> <dt>



找不到要求的項目。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR \_ NOTINITIALIZED**
</dt> <dd> <dl> <dt>



嘗試在初始化物件之前，呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 所建立之 DirectDraw 物件的介面方法。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR \_ NOTLOADED**
</dt> <dd> <dl> <dt>



介面是優化的介面，但尚未配置任何記憶體。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR \_ NOTLOCKED**
</dt> <dd> <dl> <dt>



嘗試解除鎖定未鎖定的介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**
</dt> <dd> <dl> <dt>



嘗試對沒有未處理頁面鎖定的介面進行頁面解除鎖定。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**
</dt> <dd> <dl> <dt>



所使用的介面不是以元件為基礎的介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**
</dt> <dd> <dl> <dt>



垂直空白同步處理作業沒有硬體支援。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**
</dt> <dd> <dl> <dt>



無法執行在顯示記憶體中建立 z 緩衝區或執行位區塊傳輸 (bitblt) 的作業，因為沒有適用于 z 緩衝區的硬體支援。


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**
</dt> <dd> <dl> <dt>



重迭表面不能以 z 層順序為基礎，因為硬體不支援重迭的 z 順序。


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR \_ OUTOFCAPS**
</dt> <dd> <dl> <dt>



已配置所要求操作所需的硬體。


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw 沒有足夠的記憶體來執行此作業。


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw 的顯示記憶體不足，無法執行此作業。


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**
</dt> <dd> <dl> <dt>



來源和目的地矩形位於相同的介面上，並互相重迭。


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR \_ OVERLAYCANTCLIP**
</dt> <dd> <dl> <dt>



硬體不支援裁剪的覆蓋。


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**
</dt> <dd> <dl> <dt>



嘗試在重迭上有一個以上的使用中色彩索引鍵。


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR \_ OVERLAYNOTVISIBLE**
</dt> <dd> <dl> <dt>



在隱藏的覆迭上呼叫 [**IDirectDrawSurface7：： GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) 方法。


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR \_ PALETTEBUSY**
</dt> <dd> <dl> <dt>



因為另一個執行緒已鎖定元件，所以拒絕存取這個調色板。


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**
</dt> <dd> <dl> <dt>



此進程已建立主要介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR \_ REGIONTOOSMALL**
</dt> <dd> <dl> <dt>



傳遞給 [**IDirectDrawClipper：： GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) 方法的區域太小。


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**
</dt> <dd> <dl> <dt>



嘗試將介面附加至另一個已附加的介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**
</dt> <dd> <dl> <dt>



已嘗試將介面設為與另一個介面相依的另一個介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**
</dt> <dd> <dl> <dt>



因為另一個執行緒已鎖定介面，所以會拒絕對介面的存取。


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**
</dt> <dd> <dl> <dt>



介面的存取遭到拒絕，因為介面會遮蔽。


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**
</dt> <dd> <dl> <dt>



介面的存取遭到拒絕，因為介面記憶體已消失。 在此介面上呼叫 [**IDirectDrawSurface7：： restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) 方法，以還原與其相關聯的記憶體。


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**
</dt> <dd> <dl> <dt>



未附加要求的介面。


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**
</dt> <dd> <dl> <dt>



DirectX 7.0 的新新。 當 [**IDirectDraw7：： StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) 方法傳回時，此值表示不會起始任何測試，因為所有選擇用於測試的解析度在登錄中都已有重新整理頻率資訊。 當 [**IDirectDraw7：： EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)傳回時，此值表示 DirectDraw 已完成重新整理頻率測試。


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIGHEIGHT**
</dt> <dd> <dl> <dt>



DirectDraw 要求的高度太大。


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**
</dt> <dd> <dl> <dt>



DirectDraw 要求的大小太大。 不過，個別的高度和寬度都是有效的大小。


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**
</dt> <dd> <dl> <dt>



DirectDraw 要求的寬度太大。


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**\_不支援 DDERR**
</dt> <dd> <dl> <dt>



不支援此作業。


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**
</dt> <dd> <dl> <dt>



DirectDraw 不支援要求的像素格式。


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**
</dt> <dd> <dl> <dt>



DirectDraw 不支援要求之像素格式的位元遮罩。


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ UNSUPPORTEDMODE**
</dt> <dd> <dl> <dt>



顯示目前處於不支援的模式。


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**
</dt> <dd> <dl> <dt>



垂直空白正在進行中。


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR \_ VIDEONOTACTIVE**
</dt> <dd> <dl> <dt>



影片埠未啟用。


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTILLDRAWING**
</dt> <dd> <dl> <dt>



先前正在將資訊傳送到或從此表面傳送的 bitblt 作業不完整。


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ WRONGMODE**
</dt> <dd> <dl> <dt>



因為此介面是在不同的模式中建立，所以無法還原。


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**
</dt> <dd> <dl> <dt>



提供的矩形不會在必要界限上水準對齊。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ddraw。h</dt> </dl> |



 

