---
title: 回呼函式
description: 回呼函式
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- 可安裝的驅動程式、回呼函數
- 可安裝的驅動程式，DriverCallback 函式
- 可安裝的驅動程式、事件
- DriverCallback 函式
- DRV_OPEN 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842252"
---
# <a name="callback-functions"></a>回呼函式

可安裝的驅動程式可以使用 [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) 函式，通知應用程式、視窗或開啟特定實例事件的工作。 此函式可讓驅動程式在繼續處理要求時，將資訊傳回給應用程式或 DLL 的方法。

如果驅動程式支援回呼函數，開啟實例的應用程式或 DLL 必須提供值，這是回呼函式的位址、視窗控制碼或工作控制碼。 此值和識別值型別的旗標通常會以 [**Winspool.drv \_ OPEN**](drv-open.md) message 的第二個參數所指向的結構來傳遞。

 

 