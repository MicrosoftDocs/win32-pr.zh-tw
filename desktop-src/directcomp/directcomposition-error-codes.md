---
title: 'DirectComposition 錯誤碼 (Dcomp) '
description: 本節說明 DirectComposition 特有的錯誤碼。
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d86ab61574af84e0b4b51223c69b181697dc0ebbdd7995c1bff112e286cc3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891978"
---
# <a name="directcomposition-error-codes"></a>DirectComposition 錯誤碼

如果發生錯誤，Microsoft DirectComposition 會以 **HRESULT** 值傳回程序代碼。 本節說明 DirectComposition 特有的錯誤碼。 如需 (COM) 錯誤碼的一般元件物件模型清單，請參閱 [Com 錯誤碼](/windows/desktop/com/com-error-codes)。

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_ \_ 拒絕存取 DCOMPOSITION \_ 錯誤**
</dt> <dd> <dl> <dt>


</dt> <dt>



在 [**IDCompositionDevice：： CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) 方法的呼叫中指定的視窗控制碼，屬於建立裝置物件的不同處理常式。


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**
</dt> <dd> <dl> <dt>


</dt> <dt>



當應用程式呼叫 [**IDCompositionSurface：： BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)、 [**IDCompositionSurface：： SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)或 [**IDCompositionSurface：： ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) 方法時，介面已經呈現。 如需詳細資訊，請參閱＜備註＞。


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_ \_ \_ 未 \_ \_ 呈現 DCOMPOSITION 錯誤介面**
</dt> <dd> <dl> <dt>


</dt> <dt>



應用程式針對未轉譯的介面呼叫 [**IDCompositionSurface：： SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)、 [**IDCompositionSurface：： ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)或 [**IDCompositionSurface：： EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 方法。 如需詳細資訊，請參閱＜備註＞。


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION \_ 錯誤 \_ 視窗 \_ 已 \_ 組成**
</dt> <dd> <dl> <dt>


</dt> <dt>



[**IDCompositionDevice：： CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd)方法是使用 *hwnd* 和 *最上層* 的參數（視覺化樹狀結構已存在）來呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

如果 [**IDCompositionSurface：： BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) 的呼叫是最新的動作：



| 呼叫這個方法：                                    | 傳回此值：                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ 確定                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ 確定                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_** |



 

如果 [**IDCompositionSurface：： SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) 的呼叫是最新的動作：



| 呼叫這個方法：                                    | 傳回此值：                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ 確定                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ 確定                                             |



 

如果 [**IDCompositionSurface：： ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) 的呼叫是最新的動作：



| 呼叫這個方法：                                    | 傳回此值：                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ 確定                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ 確定                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_ \_ 正在呈現 DCOMPOSITION 錯誤介面 \_ \_ 。** |



 

如果 [**IDCompositionSurface：： EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 的呼叫是最新的動作：



| 呼叫這個方法：                                    | 傳回此值：                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ 確定                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **DCOMPOSITION \_ 錯誤 \_ 介面 \_ 未 \_ \_ 呈現。** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **DCOMPOSITION \_ 錯誤 \_ 介面 \_ 未 \_ \_ 呈現。** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **DCOMPOSITION \_ 錯誤 \_ 介面 \_ 未 \_ \_ 呈現。** |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Dcomp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectComposition 參考](reference.md)
</dt> </dl>

 

