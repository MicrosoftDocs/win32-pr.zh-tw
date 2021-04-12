---
description: Merge 物件提供其他最上層物件的存取權。 必須先建立合併物件，才能載入 COM 所需的自動化支援，以存取 Mergemod.dll 中的函數。
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: 合併物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195087"
---
# <a name="merge-object"></a>合併物件

**Merge** 物件提供其他最上層物件的存取權。 必須先建立 **合併** 物件，才能載入 COM 所需的自動化支援，以存取 Mergemod.dll 中的函數。

Mergemod.dll 可在組建階段透過現有 CLSID 的第二個版本來存取擴充功能。 此 CLSID 支援透過 [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) 介面使用的現有功能，但物件 (上的預設介面和相關聯的雙重介面) 是 [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) 介面，而不是 **IMsmMerge** 介面。

 

 
