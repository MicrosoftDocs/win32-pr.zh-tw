---
description: 本節提供直接操作執行緒模型的總覽、直接操作處理視窗訊息的方式，以及區的狀態如何隨著輸入而變更，以對應至輸出動作。
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: 使用 DirectManipulation 處理輸入
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 284a0a1866a2082e2c34c65de347b0dcdfab3a64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973740"
---
# <a name="processing-input-with-directmanipulation"></a>使用 DirectManipulation 處理輸入

本節提供 [直接](direct-manipulation-portal.md) 操作執行緒模型的總覽、直接操作處理視窗訊息的方式，以及區的狀態如何隨著輸入而變更，以對應至輸出動作。

- [輸入流程](#input-flow)
- [備註](#remarks)

[直接操作](direct-manipulation-portal.md) 會使用兩個執行緒來協調非同步作業：

*UI 執行緒* -擁有與輸入相關聯之 **HWND** 的執行緒。 這個執行緒擁有 [直接操作](direct-manipulation-portal.md)的初始化。 滑鼠和鍵盤輸入處理也會在 UI 執行緒上發生。

*委派執行緒* - [直接操作](direct-manipulation-portal.md)所建立和擁有的執行緒。 觸控輸入處理會在委派執行緒上進行。

## <a name="input-flow"></a>輸入流程

在 UI 執行緒上進行點擊測試的一般 [設定中，系統會依下列](direct-manipulation-portal.md) 連續處理視窗訊息：

![顯示處理訊息的順序圖表。](images/inputprocessing.png)

針對待用的區：

1. 一連串的視窗訊息會抵達委派執行緒。
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) 和 [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) 的訊息會由委派執行緒傳送至獨立的點擊測試， (IHT) 執行緒。
3. 如果從 IHT 執行緒呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ，委派執行緒可能會將訊息傳送至 UI 執行緒，視呼叫 [**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)時的 [**DIRECTMANIPULATION \_ system.windows.media.visualtreehelper.hittest \_ 類型**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type)值而定。
4. 如果 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 不是從 IHT 執行緒呼叫，則訊息一律會由委派執行緒傳送至 UI 執行緒。
5. 用戶端可以從 UI 執行緒呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ，讓 [直接操作](direct-manipulation-portal.md) 能夠偵測操作。
6. 如果偵測到操作， [直接操作](direct-manipulation-portal.md) 會傳送 [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) 訊息，以通知用戶端由直接操作來處理輸入。 [區狀態] **設定為 [執行中]** ，輸出轉換將會更新。
7. 如果偵測到操作以外的互動， [直接操作](direct-manipulation-portal.md) 會將剩餘的訊息傳送至 UI 執行緒。

若為動作中的視口 (狀態為「執行中」或「慣性) 」，則會先將視窗訊息抵達委派執行緒，並對所有執行中的視口進行 [直接操作](direct-manipulation-portal.md) 點擊測試。 直接操作會自動將連絡人指派給點擊測試所識別的適當的區隔。 [視口] 狀態為 [執行中]，輸出轉換將會更新。

在某些情況下，應用程式 UI 執行緒可能太慢而無法回應點擊測試。 您可以使用點擊測試執行緒 ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) ，以允許用戶端將 [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) 和 [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) 訊息移至特定的執行緒，以允許進行點擊測試。

## <a name="remarks"></a>備註

一般來說， [直接操作](direct-manipulation-portal.md) 只會將 [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) 和 [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) 訊息傳送至 UI 執行緒，並在等候用戶端的回應時，于稍後將訊息提供給。 如果用戶端呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)，則偵測到操作時，UI 執行緒唯一收到的訊息為 [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) 、 [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)和 [WM/_POINTERCAPTURECHANGED 訊息](../inputmsg/wm-pointercapturechanged.md)。

處理 [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md)和 [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)訊息時，用戶端可能不會呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 。 在此情況下， [直接操作](direct-manipulation-portal.md) 會將所有訊息傳送至 UI 執行緒，而不會分析訊息以查看是否有操作。 然後，用戶端可以選擇任何點來呼叫 **SetContact** ，並讓直接操作開始偵測操作，並在偵測到一個訊息時傳送 [WM/_POINTERCAPTURECHANGED 訊息](../inputmsg/wm-pointercapturechanged.md) 訊息。

**Windows 10 和更新版本：** 您可以先呼叫 [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact)來決定要處理哪些操作，再于 [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md)或 [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)訊息上呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 。 **DeferContact** 可確保所有後續的訊息都會在指定的時間內傳送至 UI 執行緒。
