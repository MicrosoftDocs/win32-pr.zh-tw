---
title: 載入字元
description: 載入字元
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78d796df5c1699b405e8cae1dbae0e7d7d8d37932aa50534fa7331a458dc54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748401"
---
# <a name="loading-a-character"></a>載入字元

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

若要建立字元的動畫，您必須先載入該字元。 使用 [**load**](load-method.md) 方法載入字元的資料。 Microsoft Agent 支援兩種格式的字元和動畫資料：單一結構化檔案和不同的檔案。 一般而言，您會使用單一檔案格式 (。當資料儲存在本機時，ACS) 。  ( 的多個檔案格式。ACF。當您想要個別下載動畫時（例如從 HTTP 伺服器存取動畫時），ACA) 的效果最佳。

用戶端應用程式只能載入相同字元的單一實例。 嘗試多次載入相同字元將會失敗。 不過，應用程式可以透過提供與 Microsoft Agent 的個別連接，來載入相同字元的多個實例。 例如，應用程式可以從 Microsoft Agent 控制項的兩個複本載入相同的字元。

您也可以定義您自己的字元以搭配 Microsoft Agent 使用。 您可以使用任何偏好的轉譯工具來建立影像，但前提是您最後會得到 Windows 點陣圖格式檔案。 若要組合字元的影像並將其編譯成可搭配 Microsoft Agent 使用的動畫，請使用 Microsoft Agent 字元編輯器。 此工具可讓您定義字元的預設屬性，以及定義字元的動畫。 當您建立字元時，Microsoft 代理程式字元編輯器也可讓您選取適當的檔案格式。

 

 




