---
title: 載入字元
description: 載入字元
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673119"
---
# <a name="loading-a-character"></a>載入字元

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

若要建立字元的動畫，您必須先載入該字元。 使用 [**load**](load-method.md) 方法載入字元的資料。 Microsoft Agent 支援兩種格式的字元和動畫資料：單一結構化檔案和不同的檔案。 一般而言，您會使用單一檔案格式 (。當資料儲存在本機時，ACS) 。  ( 的多個檔案格式。Acf。當您想要個別下載動畫時（例如從 HTTP 伺服器存取動畫時），ACA) 的效果最佳。

用戶端應用程式只能載入相同字元的單一實例。 嘗試多次載入相同字元將會失敗。 不過，應用程式可以透過提供與 Microsoft Agent 的個別連接，來載入相同字元的多個實例。 例如，應用程式可以從 Microsoft Agent 控制項的兩個複本載入相同的字元。

您也可以定義您自己的字元以搭配 Microsoft Agent 使用。 您可以使用任何偏好的轉譯工具來建立影像，但最後您會得到 Windows 點陣圖格式檔案。 若要組合字元的影像並將其編譯成可搭配 Microsoft Agent 使用的動畫，請使用 Microsoft Agent 字元編輯器。 此工具可讓您定義字元的預設屬性，以及定義字元的動畫。 當您建立字元時，Microsoft 代理程式字元編輯器也可讓您選取適當的檔案格式。

 

 




