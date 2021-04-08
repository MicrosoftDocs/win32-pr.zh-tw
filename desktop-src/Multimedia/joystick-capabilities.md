---
title: 搖桿功能
description: 搖桿功能
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- 多媒體輸入，操縱杆
- 操縱杆、雙軸移動
- 操縱杆，三軸移動
- 操縱杆，按鈕
- 操縱杆，移動的範圍
- 操縱杆，輪詢頻率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682212"
---
# <a name="joystick-capabilities"></a>搖桿功能

搖桿可以支援兩個或三個軸的移動，最多可支援四個按鈕。 操縱杆也支援不同 *範圍的動作* 和 *輪詢頻率*。 動作的範圍是搖桿控點可以從其停留位置移至最遠距離其停留位置的距離。 輪詢頻率是操縱杆查詢之間的時間間隔。

搖桿驅動程式可支援一或兩個操縱杆。 您可以使用 [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) 函式來判斷搖桿驅動程式支援的搖桿數目。 此函式會傳回不帶正負號的整數，其中包含支援的操縱杆或零（如果沒有搖桿支援的話）。 傳回值不會指出附加至系統的搖桿數目。

您可以使用 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 函式來判斷搖桿是否已附加至系統。 \_如果已附加指定的裝置，此函數會傳回 JOYERR >aad-userreadusingalternativesecurityid-noerror。 否則，它會傳回已 JOYERR 的已插即用 \_ 。

每個搖桿都有數個可供您的應用程式使用的功能。 您可以使用 [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) 函式來取出搖桿的功能。 此函式會以搖桿功能填滿 [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) 結構，例如其座標系統的最小值和最大值、搖桿上的按鈕數目，以及最小和最大輪詢頻率。

 

 