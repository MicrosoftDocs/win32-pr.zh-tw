---
title: 準備您的應用程式以進行64位 Windows
description: 有幾項功能可讓您更輕鬆地開發將在32和64位 Windows 上執行的應用程式。 其中大部分的（例如新的資料類型）都是在準備進行64位 Windows 時所述。
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64位工具組64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6c8d31b685e6f545aca4bdaac341fe25a3c96f458048808536899a8416120a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071618"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>準備您的應用程式以進行64位 Windows

有幾項功能可讓您更輕鬆地開發將在32和64位 Windows 上執行的應用程式。 其中大部分的（例如新的資料類型）都是在[準備進行64位 Windows](getting-ready-for-64-bit-windows.md)時所述。

隨附于 Windows SDK 的64位工具組包含64位 MIDL 編譯器，Midl.exe，用於產生原生64位的存根以及32位的存根。 使用 **/env win64** 參數只產生64位的存根。 預設值是產生兩個平臺上執行的雙重存根。

請注意，64位 MIDL 只支援 [**/Oicf**](/windows/desktop/Midl/-oi) 和 [**/os**](/windows/desktop/Midl/-os) 優化模式。

 

 