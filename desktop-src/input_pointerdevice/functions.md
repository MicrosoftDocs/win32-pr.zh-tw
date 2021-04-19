---
description: 本節中的主題提供指標裝置輸入堆疊函數的參考規格。
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: '函數 (指標裝置輸入堆疊) '
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106993691"
---
# <a name="pointer-device-input-stack-functions"></a>指標裝置輸入堆疊函數

本節中的主題提供 [指標裝置輸入堆疊](pointer-device-stack-portal.md) 函數的參考規格。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | 設定呼叫應用程式的指標插入裝置，並初始化應用程式可以插入的同時指標數目上限。<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | 終結指定的指標插入裝置。<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | 取得指標裝置的相關資訊。<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | 取得對應至與指標裝置相關聯之資料指標的資料指標識別碼。<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | 取得不包含在 [**指標 \_ 裝置 \_ 資訊**](/previous-versions/windows/desktop/api) 結構中的裝置屬性。 <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | 取得指標裝置 (在 himetric) 中的 x 和 y 範圍，以及指標裝置所對應之顯示的 x 和 y 範圍 (目前的解析度) 。 <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | 取得連接到系統之指標裝置的相關資訊。<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | 從指標裝置取得原始輸入資料。 <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | 模擬指標輸入 (畫筆或觸控) 。<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | 註冊視窗，以處理 [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md)、 [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)和 [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) 指標裝置通知。<br/> |

## <a name="related-topics"></a>相關主題

[指標裝置輸入堆疊參考](unified-input-stack-reference.md)
