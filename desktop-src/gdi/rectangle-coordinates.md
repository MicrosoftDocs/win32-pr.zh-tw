---
description: 應用程式必須使用 RECT 結構來定義矩形。
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: 矩形座標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991174"
---
# <a name="rectangle-coordinates"></a>矩形座標

應用程式必須使用 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構來定義矩形。 結構會指定兩個點的座標：矩形的左上角和右下角。 矩形的側邊會從這兩個點延伸，並且平行至 X 軸和 y 軸。

矩形的座標值會以帶正負號的整數表示。 矩形右邊的座標值必須大於其左邊的座標值。 同樣地，底部的座標值必須大於頂端的座標值。

由於應用程式可以將矩形用於許多不同的用途，因此矩形函式不會使用明確的測量單位。 相反地，所有的矩形座標和維度都會以帶正負號的邏輯值提供。 對應模式和使用該矩形的函式會決定測量單位。 如需座標和對應模式的詳細資訊，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。

 

 
