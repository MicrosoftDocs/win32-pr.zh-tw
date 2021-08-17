---
description: 色板是一個陣列，其中包含的色彩值會識別目前可在輸出裝置上顯示或繪製的色彩。
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: '色彩調色板 (Windows GDI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81079ac94b40de98bc1c53098a8b9d1654f90d0d855397ac38d11311e9741e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761955"
---
# <a name="color-palettes-windows-gdi"></a>色彩調色板 (Windows GDI) 

色板是一個陣列，其中包含的色彩值會識別目前可在輸出裝置上顯示或繪製的色彩。 色彩調色板是由能夠產生許多色彩的裝置所使用，但在任何指定時間只能顯示或繪製這些色彩的子集。 針對這類裝置，系統會維護 *系統元件* ，以追蹤和管理裝置目前的色彩。 應用程式無法直接存取系統調色板。 相反地，系統會將預設的調色板與每個裝置內容產生關聯。 應用程式可以使用預設調色板中的色彩，或藉由建立 *邏輯調色板* 並將它們與個別裝置內容產生關聯，來定義自己的色彩。

應用程式可以 \_ 在 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式所傳回的 RASTERCAPS 值中檢查 RC 選擇區位，藉以判斷裝置是否支援色彩調色板。

 

 



