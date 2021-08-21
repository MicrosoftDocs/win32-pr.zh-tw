---
description: 當使用者按一下 [視窗] 功能表中的 [最小化]，或應用程式呼叫 ShowWindow 函式並指定值（例如 SW 最小化）時，系統會將應用程式的主視窗減少 (重迭樣式) 至最小化的視窗 \_ 。
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: 最小化 Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9633c3bcba452e4708c6a48557fe547eff03c4e2a6801e3669da2faa768272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760028"
---
# <a name="minimized-windows"></a>最小化 Windows

當使用者按一下 [視窗] 功能表中的 [最小化]，或應用程式呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式並指定值（例如 SW \_ 最小化）時，系統會將應用程式的主視窗減少 (重迭樣式) 至最小化的視窗。 將視窗最小化可減少應用程式在更新主視窗時必須執行的工作量，以加速系統效能。

若為一般應用程式，系統會在視窗最小化時，繪製稱為類別圖示的圖示，並以視窗的名稱標記圖示。 類別圖示（代表應用程式的靜態影像）是由應用程式在註冊視窗類別時所指定。 應用程式會在呼叫 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)之前，將控制碼指派給 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)的 **hIcon** 成員。 應用程式可以使用 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) 函式來取出圖示控制碼。

 

 
