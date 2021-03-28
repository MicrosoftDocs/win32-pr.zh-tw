---
description: ExcludeUpdateRgn 函式會從顯示裝置內容的裁剪區域中排除更新區域。
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: 排除更新區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026458"
---
# <a name="excluding-the-update-region"></a>排除更新區域

[**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)函式會從顯示裝置內容的裁剪區域中排除更新區域。 當您在非 WM \_ 油漆訊息正在處理的視窗中繪製時，此函式很有用。 它會防止在下一個 WM 油漆訊息期間更新的區域中進行繪圖 \_ 。

 

 



