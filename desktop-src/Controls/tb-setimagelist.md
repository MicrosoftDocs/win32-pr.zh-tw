---
title: 'TB_SETIMAGELIST 訊息 (Commctrl .h) '
description: 設定工具列用來顯示處於預設狀態之按鈕的影像清單。
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- TB_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969186"
---
# <a name="tb_setimagelist-message"></a>TB \_ SETIMAGELIST 訊息

設定工具列用來顯示處於預設狀態之按鈕的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[版本5.80。](common-control-versions.md) 清單的索引。 如果您只使用一個影像清單或較舊版本的通用控制項，請將 *wParam* 設定為零。 如需使用多個影像清單的詳細資訊，請參閱備註。

</dd> <dt>

*lParam* 
</dt> <dd>

要設定之影像清單的控制碼。 如果此參數為 **Null**，則不會在按鈕中顯示任何影像。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回影像清單的控制碼，此控制碼先前可用來顯示其預設狀態下的按鈕; 如果沒有先前設定的影像清單，則為 **Null** 。

## <a name="remarks"></a>備註

> [!Note]  
> 您的應用程式會負責在工具列損毀之後釋放影像清單。

 

**Tb 的 \_ SETIMAGELIST** 訊息無法與 [**tb \_ ADDBITMAP**](tb-addbitmap.md)結合。 它也不能與以 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)建立的工具列搭配使用，它會在內部呼叫 **TB 的 \_ ADDBITMAP** 。 當您使用 **CreateToolbarEx** 建立工具列或使用 **TB \_ ADDBITMAP** 來加入影像時，工具列會在內部管理影像清單。 嘗試以 **TB \_ SETIMAGELIST** 進行修改，會產生無法預期的結果。

使用 [5.80 版](common-control-versions.md) 或更新版本的通用控制項，按鈕影像不需要來自相同的影像清單。 若要針對您的工具列按鈕影像使用多個影像清單：

1.  藉由使用 *wParam* 將 [**CCM \_ SETVERSION**](ccm-setversion.md)訊息傳送給工具列控制項，以啟用多個影像清單， () 設定為5的版本號碼。
2.  針對您想要使用的每個影像清單，將 [工具列] 控制項傳送至 [ **TB] \_ SETIMAGELIST** 訊息。 將 *wParam* 設定為將用來識別清單的應用程式定義 *wParam* 值。 將 *lParam* 設定為清單的 HIMAGELIST 控制碼。
3.  針對每個按鈕，將按鈕 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **iBitmap** 成員設定為 MAKELONG (*iIndex*， *iImageID*) 。 *IImageID* 值是在步驟2中定義的適當影像清單的識別碼。 *IIndex* 值是該清單中特定影像的索引。
4.  藉由將工具列控制項傳送至 TB 的 [**\_ ADDBUTTONS**](tb-addbuttons.md) 訊息來新增按鈕。

下列程式碼片段說明如何將五個按鈕加入至工具列，其中包含三個不同影像清單中的影像。 對多個映射清單的支援會透過 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息啟用。 然後，會設定並指派識別碼為0-2 的影像清單。 按鈕是從影像清單中指派影像，如下所示：

-   按鈕0是來自影像清單零 (ahim \[ 0 \]) 索引為1。
-   按鈕1是來自影像清單一 (ahim \[ 1 \]) 索引為1。
-   按鈕2是來自影像清單兩 (ahim \[ 2 \]) 索引為1。
-   按鈕3是來自影像清單零 (ahim \[ 0 \]) ，索引為2。
-   按鈕4來自 [影像清單 1] (ahim \[ 1 \]) 索引為3。

最後，按鈕會新增至具有 [**TB \_ ADDBUTTONS**](tb-addbuttons.md) 訊息的工具列控制項。


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

