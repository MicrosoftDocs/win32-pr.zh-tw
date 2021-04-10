---
title: DWM 函數
description: 本節包含桌面視窗管理員 (DWM) 函數的相關資訊。
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- 桌面視窗管理員 (DWM) ，參考
- DWM (桌面視窗管理員) ，參考
- 桌面視窗管理員 (DWM) 、函數
- DWM (桌面視窗管理員) ，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316603"
---
# <a name="dwm-functions"></a>DWM 函數

本節包含桌面視窗管理員 (DWM) 函數的相關資訊。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br/></td>
<td>此函數並未實作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>非工作區中 DWM 點擊測試的預設視窗程式。<br/> 您也必須確保針對<a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a>訊息呼叫<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> 。 如果未針對<strong>WM_NCMOUSELEAVE</strong>訊息呼叫<strong>DwmDefWindowProc</strong> ，當游標離開視窗時，DWM 不會從 [<strong>最大化</strong>]、[<strong>最小化</strong>] 和 [<strong>關閉</strong>] 按鈕中移除反白顯示。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>此函數並未實作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>啟用指定之視窗的模糊效果。<br/></td>
<b>注意</b> 從 Windows 8 開始，呼叫此函式並不會造成模糊效果，因為轉譯視窗的方式中的樣式變更。
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>啟用或停用 DWM 組合。 <br/>
<blockquote>
[!Note]<br />
從 Windows 8 起，此函式已被取代。 DWM 無法再以程式設計的方式停用。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>通知 DWM 在呼叫進程運作時，加入宣告或退出多媒體類別排程服務 (MMCSS) 排程。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>將視窗框架擴充到工作區。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>發出排清呼叫，在所有目前未完成的 Microsoft DirectX 介面更新完成時，封鎖呼叫端直到下一次出現為止。 這會針對非常複雜的場景進行補償，或以非常低的優先順序呼叫處理常式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>抓取用於 DWM 玻璃組合的目前色彩。 這個值是以目前的色彩配置為基礎，而且可由使用者進行修改。 應用程式可以藉由處理 <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> 通知來接聽色彩變更。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>抓取所指定視窗的目前組合計時資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br/></td>
<td>此函數並未實作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br/></td>
<td>此函數並未實作。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br/></td>
<td>捕獲傳輸屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>注意</strong>  這個函式是公開可用的，但無法正常運作，Windows 10 版本1803。
</blockquote>
檢查在指定的視窗的應用程式標題列中取得索引標籤所需的需求。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>抓取套用至視窗之指定屬性的目前值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>由應用程式呼叫，以指出所有先前從視窗提供的 iconic 點陣圖（縮圖和查看表示）都應該重新整理。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>取得值，這個值會指出是否已啟用 DWM 組合。 執行 Windows 7 或更早版本之電腦上的應用程式，可以藉由處理 <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> 通知，來接聽撰寫狀態變更。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>變更將顯示上一個畫面格的監視器重新整理次數。 <br/> 不再支援<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> 。 從 Windows 8.1 開始，對 <strong>DwmModifyPreviousDxFrameDuration</strong> 的呼叫一律會傳回 E_NOTIMPL。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>捕獲 DWM 縮圖的來源大小。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>建立目的地和來源視窗之間的 DWM 縮圖關聯性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>通知 DWM，觸控連絡人已被辨識為手勢，而且 DWM 應該繪製該手勢的意見反應。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>設定用來顯示所呈現畫面格的監視器重新整理數目。 <br/> 不再支援<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> 。 從 Windows 8.1 開始，對 <strong>DwmSetDxFrameDuration</strong> 的呼叫一律會傳回 E_NOTIMPL。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>設定靜態的 iconic 點陣圖以顯示 <em>即時預覽</em> (也稱為視窗或索引標籤的 [ <em>查看預覽</em> ]) 。工作列可以使用此點陣圖來顯示視窗或索引標籤的完整大小預覽。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>在視窗或索引標籤上設定靜態、iconic 點陣圖，以做為縮圖標記法。 工作列可以使用此點陣圖作為視窗或索引標籤的縮圖切換目標。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>設定框架組合的目前參數。 <br/> 不再支援<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> 。 從 Windows 8.1 開始，對 <strong>DwmSetPresentParameters</strong> 的呼叫一律會傳回 E_NOTIMPL。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>設定視窗的非用戶端轉譯屬性值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>由應用程式或架構呼叫，以指定要繪製以回應特定觸控或畫筆連絡人的視覺效果意見反應類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>啟用觸控和拖曳互動至使用者的圖形化意見反應。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>使用 DWM 來協調工具視窗的動畫。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>移除 <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> 函數所建立的 DWM 縮圖關聯性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>更新 DWM 縮圖的屬性。<br/></td>
</tr>
</tbody>
</table>



 

 

