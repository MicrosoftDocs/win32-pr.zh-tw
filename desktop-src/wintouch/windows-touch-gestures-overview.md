---
title: Windows觸控手勢總覽
description: 本節說明 Windows Touch 支援的各種手勢。
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows觸控、手勢
- 手勢，關於
- WindowsTouch，舊版支援
- 手勢，舊版支援
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: f2a0f6229afe4ad0d894a1cc2d40489f5d8371de3d7c42cefdccde619119df75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587250"
---
# <a name="windows-touch-gestures-overview"></a>Windows觸控手勢總覽

本節說明 Windows Touch 支援的各種手勢。

## <a name="gestures-overview"></a>手勢總覽

Windows觸控可啟用數個支援單一和多個連絡人的手勢。 下圖說明 Windows 7 中支援的各種手勢。

![圖例顯示 windows 7 中 windows 觸控支援的手勢](images/gestures.png)

> [!Note]  
> 當連絡人彼此分開時，某些辨識器會更可靠地解讀具有多個連絡人的手勢。

## <a name="legacy-support"></a>舊版支援

針對舊版支援，預設的軌跡處理常式會對應一些手勢，以 Windows 舊版 Windows 中所使用的訊息。 下表概述手勢如何對應至舊版訊息。

| 手勢        | 描述  | 產生的訊息 ()               |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 移動瀏覽            | 平移手勢會對應到使用滾輪。                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| 按住 | 按住手勢會對應到以滑鼠右鍵按一下滑鼠。     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | 縮放手勢會觸發類似于按住 CTRL 鍵的訊息，並將滑鼠滾輪旋轉以滾動。 | 在 *lParam* 中設定 **MK_CONTROL** 的 **WM_MOUSEWHEEL** |

## <a name="interpreting-windows-touch-gestures"></a>解讀 Windows Touch 手勢

Windows應用程式開發人員可以藉由處理來自應用程式 WndProc 函式的 [**WM_GESTURE**](wm-gesture.md)訊息來解讀觸控手勢。 處理此訊息之後，您可以取得描述手勢的 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) 結構。 **GESTUREINFO** 結構將會有依手勢類型而定的各種資訊。

藉由將手勢資訊結構的控制碼傳遞至 [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)函式，即可取出 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)結構。

下列旗標表示手勢的各種狀態，並儲存在 *dwFlags* 中。 

| 名稱        | 值      | 描述                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | 正在開始手勢。           |
| GF_INERTIA | 0x00000002 | 筆勢已觸發慣性。 |
| GF_END     | 0x00000004 | 筆勢已完成。          |

> [!Note]  
> 大部分的應用程式應該忽略 **GID_BEGIN** 並 **GID_END** ，然後將其傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)。 這些訊息會由預設的軌跡處理常式使用。 當協力廠商應用程式取用 **GID_BEGIN** 和 **GID_END** 訊息時，不會定義應用程式行為。

下表指出筆勢的各種識別碼。 

| 名稱              | 值 | 描述                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | 正在開始手勢。      |
| GID_END          | 2     | 手勢正在結束。        |
| GID_ZOOM         | 3     | 縮放手勢。           |
| GID_PAN          | 4     | 平移手勢。            |
| GID_ROTATE       | 5     | 旋轉手勢。       |
| GID_TWOFINGERTAP | 6     | 雙向點一下手勢。 |
| GID_PRESSANDTAP  | 7     | 按下和點擊手勢。  |

> [!Note]  
> **GID_PAN** 手勢有內建的慣性。 在平移手勢結束時，其他的平移手勢訊息是由作業系統所建立。

[**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)結構成員 **ptsLocation** 和 **ullArguments** 會使用 **點** 結構) 指定點 (，並根據手勢來指定筆勢的其他相關資訊。 下表列出與每個手勢類型相關聯的值。

| 手勢識別碼            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | 表示兩個點之間的距離。            | 指出縮放的中心。   |
| **GID_PAN**          | 表示兩個點之間的距離。            | 表示平移的目前位置。                    |
| **GID_ROTATE**       | 指出如果已設定 **GF_BEGIN** 旗標，則為旋轉的角度。 否則，這是自旋轉開始之後的角度變化。 這會經過簽署，以指出旋轉的方向。 使用 [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) 並 [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) 宏來取得和設定角度值。 | 這表示旋轉的中心，也就是目標物件周圍旋轉的靜止點。 |
| **GID_TWOFINGERTAP** | 表示兩個手指之間的距離。           | 表示雙手指的中心。                      |
| **GID_PRESSANDTAP**  | 指出第一個手指和第二個手指之間的差異。 這個值會儲存在 *ullArguments* 成員之較低32位的 **點** 結構中。                        | 指出第一個手指關閉的位置。   |

## <a name="related-topics"></a>相關主題

[Windows觸控手勢](guide-multi-touch-gestures.md)