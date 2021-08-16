---
description: GetUpdateRect 和 GetUpdateRgn 函式會取出視窗的目前更新區域。
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: 正在抓取更新區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28bf72bfcfd28ec0fc9a90485a94e19d0514bb0206de660c11a56d12f33671e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698241"
---
# <a name="retrieving-the-update-region"></a>正在抓取更新區域

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)和 [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)函式會取出視窗的目前更新區域。 GetUpdateRect 會) 括住整個更新區域的邏輯座標 (抓取最小的矩形。 GetUpdateRgn 會捕獲更新區域本身。 這些函式可用來計算更新區域的目前大小，以決定要執行繪圖作業的位置。

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)也會抓取封閉目前更新區域之最小矩形的維度，將維度複製到 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)結構中的 **rcPaint** 成員。 因為 **BeginPaint** 會驗證更新區域，所以在呼叫 **BeginPaint** 之後立即呼叫 [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)和 [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)會傳回空的更新區域。

 

 



