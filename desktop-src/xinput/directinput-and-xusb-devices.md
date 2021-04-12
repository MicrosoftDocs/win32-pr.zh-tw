---
title: DirectInput 和 XUSB 裝置
description: Xbox 通用控制器類別的驅動程式 (Windows 上的 XUSB) 會為 XINPUT DLL 執行核心模式介面。
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2b6d2857502c0e0209d94fb6d933618c180fd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316330"
---
# <a name="directinput-and-xusb-devices"></a>DirectInput 和 XUSB 裝置

Xbox 通用控制器類別的驅動程式 (Windows 上的 XUSB) 會為 XINPUT DLL 執行核心模式介面。 為了針對搭配通用控制器裝置使用 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) API 的舊版標題提供良好的體驗，驅動程式也會匯出) 類別介面 (隱藏的人介面裝置，該介面是由 DirectInput 所挑選。 我們根據原始 XINPUT 版本的一組遊戲應用程式中的一般行為，選擇 XUSB 到 HID 的對應，並且更新了較新子類型的對應。 本主題說明對應。

## <a name="human-interface-device-hid"></a>人性化介面裝置 (HID)

HID 標準是通用序列匯流排 (USB) 委員會最初建議的標準，可將輸入裝置的通訊協定一般化。 它是由一個位元組程式碼描述語言所組成，可以表達 gamepads、老鼠、操縱杆、節流閥和方向舵控制項，以及多軸控制器。 因為這是一般化的標準，所以您可能難以撰寫使用來自任意裝置輸入的軟體。 因此，針對以遊戲為中心的 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) API，我們開發了類型的特定子對應，以鼓勵硬體製造商透過其驅動程式支援。

- [適用于 HID 的 USB 裝置類別定義-1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> 您也可以透過 [RAWINPUT API](../inputdev/about-raw-input.md) 存取隱藏的輸入裝置，並透過低層級的 [HID API](/windows-hardware/drivers/hid/introduction-to-hid-concepts) 處理輸入報告，但振動的意見反應將無法像 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))一樣運作。

## <a name="mappings"></a>對應

XUSB 驅動程式會同時針對裝置同時執行 XUSB 類別介面和 HID 類別介面，以支援 XINPUT 和 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) 的使用方式。 此對應是根據 XUSB 子類型資訊。 驅動程式會執行四個不同的對應群組。

| XUSB 子類型                                      | 對應                     |
|---------------------------------------------------|-----------------------------|
| XINPUT \_ DEVSUBTYPE \_ 遊戲 (子類型 1)            | 遊戲台                     |
| XINPUT \_ DEVSUBTYPE \_ 輪子 (子類型 2)              | Wheel                       |
| XINPUT \_ DEVSUBTYPE \_ ARCADE \_ 搖杆 (子類型 3)      | Arcade 搖杆/Arcade Pad     |
| XINPUT \_ DEVSUBTYPE \_ 飛行 \_ 杆 (子類型 4)      | 飛行杆                |
| XINPUT \_ DEVSUBTYPE \_ DANCE \_ PAD (子類型 5)         | 任何新子型別的預設值 |
| XINPUT \_ DEVSUBTYPE \_ 吉他 (子類型 6)             | 吉他                      |
| XINPUT \_ DEVSUBTYPE \_ 吉他 \_ 替代 (子類型 7)  |                             |
| XINPUT \_ DEVSUBTYPE \_ 鼓 \_ 套件 (子類型 8)          |                             |
| XINPUT \_ DEVSUBTYPE \_ 吉他 \_ 低音 (子類型 11)      |                             |
| XINPUT \_ DEVSUBTYPE \_ ARCADE \_ PAD (子類型 19)       |                             |

> [!Note]  
> 下列隱藏的對應是靜態的。 這表示即使裝置功能報告指出不支援特定的按鈕或軸，該對應仍會包含它，但一律會報告關閉狀態或置中值。

## <a name="gamepad"></a>遊戲台

這是預設的對應，並且是設計在標準 Xbox 通用控制器遊戲台的周圍，並公開為 *遊戲台* HID 使用類型。

| 控制                      | HID 使用名稱 | 使用量頁面 | 使用識別碼   |
|------------------------------|----------------|------------|------------|
| 左搖杆                   | X，Y           | 0x01       | 0x30<、0x31 |
| 右搖杆                  | Rx、Ry         | 0x01       | 0x33, 0x34 |
| 左方觸發程式 + 右觸發程式 | Z\*            | 0x01       | 0x32       |
| D-向上、向下、向左、靠右  | Hat 參數     | 0x01       | 0x39       |
| A                            | 按鈕1       | 0x09       | 0x01       |
| B                            | 按鈕2       | 0x09       | 0x02       |
| X                            | 按鈕3       | 0x09       | 0x03       |
| Y                            | 按鈕4       | 0x09       | 0x04       |
| LB (左緩衝)              | 按鈕5       | 0x09       | 0x05       |
| RB (右緩衝器)             | 按鈕6       | 0x09       | 0x06       |
| 返回                         | 按鈕7       | 0x09       | 0x07       |
| START                        | 按鈕8       | 0x09       | 0x08       |
| LSB (左搖杆按鈕)       | 按鈕9       | 0x09       | 0x09       |
| RSB (右搖杆按鈕)      | 按鈕10      | 0x09       | 0x0A       |

> [!Note]  
>  (\*) ：這會結合，因此 Z 會顯示旋轉大部分標題所預期的集中行為，這表示無法透過 [DIRECTINPUT](/previous-versions/windows/desktop/ee416842(v=vs.85)) 和 HID 查看所有可能的觸發程式組合值。

## <a name="arcade-stickarcade-pad"></a>Arcade 搖杆/Arcade Pad

這是以 Arcade 杆控制器為中心所設計的對應，並公開為 *遊戲* 程式的 HID 使用類型。 Arcade Pad 非常類似 Arcade，但以較小的外型規格為准。 這些設計會以報告最小和最大軸值的數位按鈕，取代類比左方觸發程式和右觸發程式。

| 控制                     | HID 使用名稱 | 使用量頁面 | 使用識別碼 |
|-----------------------------|----------------|------------|----------|
| D-向上、向下、向左、靠右 | Hat 參數     | 0x01       | 0x39     |
| A                           | 按鈕1       | 0x09       | 0x01     |
| B                           | 按鈕2       | 0x09       | 0x02     |
| X                           | 按鈕3       | 0x09       | 0x03     |
| Y                           | 按鈕4       | 0x09       | 0x04     |
| LB (左緩衝)             | 按鈕5       | 0x09       | 0x05     |
| RB (右緩衝器)            | 按鈕6       | 0x09       | 0x06     |
| 返回                        | 按鈕7       | 0x09       | 0x07     |
| START                       | 按鈕8       | 0x09       | 0x08     |
| 左方觸發程式                | 按鈕9       | 0x09       | 0x09     |
| 右觸發程式               | 按鈕10      | 0x09       | 0x0A     |

這些裝置不一定支援其他控制項，但它們不是由隱藏的隱藏：左方、右下角、LSB (左移按鈕) ，以及 RSB (右下角按鈕) 。

## <a name="wheel"></a>Wheel

這項地圖設計圍繞 Xbox 賽車，並公開為 *遊戲* 程式的 HID 使用類型。

| 控制                                                        | HID 使用名稱 | 使用量頁面 | 使用識別碼 |
|----------------------------------------------------------------|----------------|------------|----------|
| 滾輪 (左搖杆 X)                                            | X              | 0x01       | 0x30     |
|  (右觸發程式的加速器踏板) + 煞車踏板 (左方觸發程式)  | Z\*            | 0x01       | 0x32     |
| D-向上、向下、向左、靠右                                    | Hat 參數     | 0x01       | 0x39     |
| A                                                              | 按鈕1       | 0x09       | 0x01     |
| B                                                              | 按鈕2       | 0x09       | 0x02     |
| X                                                              | 按鈕3       | 0x09       | 0x03     |
| Y                                                              | 按鈕4       | 0x09       | 0x04     |
| LB (左緩衝)                                                | 按鈕5       | 0x09       | 0x05     |
| RB (右緩衝器)                                               | 按鈕6       | 0x09       | 0x06     |
| LSB (左搖杆按鈕)                                         | 按鈕7       | 0x09       | 0x07     |
| RSB (右搖杆按鈕)                                        | 按鈕8       | 0x09       | 0x08     |
| 返回                                                           | 按鈕9       | 0x09       | 0x09     |
| START                                                          | 按鈕10      | 0x09       | 0x0A     |

> [!Note]  
>  (\*) ：這會合並，讓 Z 顯示煞車和快速鍵控制項的大部分標題所預期的集中行為; 這表示無法透過 [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))查看所有可能的踏板組合值。

## <a name="flight-stick"></a>飛行杆

此對應是圍繞 Xbox 飛行杆所設計，並公開為 *搖桿* 隱藏使用類型。

| 控制                     | 使用名稱 | 使用量頁面 | 使用識別碼   |
|-----------------------------|------------|------------|------------|
| 飛行杆 (左搖杆)    | X，Y       | 0x01       | 0x30<、0x31 |
| POV Hat (右搖杆)        | Rx、Ry     | 0x01       | 0x33, 0x34 |
|  (右觸發程式的節流)     | Z          | 0x01       | 0x32       |
| 左方觸發程式的方向 ()        | Rz         | 0x01       | 0x35        |
| D-向上、向下、向左、靠右 | Hat 參數 | 0x01       | 0x39       |
| 主要武器 ()           | 按鈕1   | 0x09       | 0x01       |
| 次要武器 (B)         | 按鈕2   | 0x09       | 0x02       |
| X                           | 按鈕3   | 0x09       | 0x03       |
| Y                           | 按鈕4   | 0x09       | 0x04       |
| LB (左緩衝)             | 按鈕5   | 0x09       | 0x05       |
| RB (右緩衝器)            | 按鈕6   | 0x09       | 0x06       |
| 返回                        | 按鈕7   | 0x09       | 0x07       |
| START                       | 按鈕8   | 0x09       | 0x08       |
| LSB (左搖杆按鈕)      | 按鈕9   | 0x09       | 0x09       |
| RSB (右搖杆按鈕)     | 按鈕10  | 0x09       | 0x0A       |

> [!Note]  
> 這是以最終飛行杆設計為基礎。 因為這與早期飛行杆定義不同，所以許多裝置都有支援舊的和新模型的模式切換。 此對應會假設新的模型。