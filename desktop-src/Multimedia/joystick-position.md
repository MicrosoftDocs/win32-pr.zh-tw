---
title: 搖桿位置
description: 搖桿位置
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- 操縱杆、位置
- 操縱杆，按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e5664166d20f9195a33d03534f792a4262b291bc3db34194fd05e06681563a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140302"
---
# <a name="joystick-position"></a>搖桿位置

您可以使用 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 函式，查詢搖桿是否有位置和按鈕資訊。 例如，應用程式可以查詢搖桿的基準位置值。 在校正搖桿時，[操縱杆主控台] 屬性工作表會使用這項技術。

您也可以使用 [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) 函式，查詢具有擴充功能的搖桿或其他裝置。

 

 