---
description: PDH 定義下列資料類型。
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: 效能計數器資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989405"
---
# <a name="performance-counters-data-types"></a>效能計數器資料類型

## <a name="performance-data-helper-pdh-types"></a>效能資料協助程式 (PDH) 類型

使用 [效能資料協助程式 (PDH) ](using-the-pdh-functions-to-consume-counter-data.md) 函數的取用者會使用下列類型：

| 資料類型 | 描述
|-----------|------------
| **PDH \_ HQUERY**   | 查詢的控制碼。 [**PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw)函式會傳回這個控制碼。 使用 [**PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery)關閉控制碼。
| **PDH \_ HCOUNTER** | 計數器的控制碼。 [**PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw)函式會傳回這個控制碼。 使用 [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) 關閉控制碼，或關閉包含計數器的查詢控制碼。 如果對應的查詢已經關閉，請勿在計數器上呼叫 **PdhRemoveCounter** 。 PDH 會維護計數器和查詢之間的連結，並且在對應的查詢控制碼關閉時，自動關閉計數器控制碼。
| **PDH \_ HLOG**     | 記錄檔的控制碼。 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)和 [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)函數會傳回此控制碼。 使用 [**PdhCloseLog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog)關閉控制碼。
| **PDH \_ 狀態**   | PDH 狀態值。 所有 PDH 函數都會傳回類型為 **PDH 的 \_** 值。 如果函式成功，則傳回值為「錯誤 \_ 成功」。 否則，函數會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。
