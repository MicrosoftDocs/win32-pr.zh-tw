---
title: BC-VCM-LVM-HYPERV 架構
description: BC-VCM-LVM-HYPERV 架構
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- 適用于 Windows (VFW) ，BC-VCM-LVM-HYPERV 架構的影片
- 適用于 Windows) 的 VFW (影片，BC-VCM-LVM-HYPERV 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301407"
---
# <a name="vcm-architecture"></a>BC-VCM-LVM-HYPERV 架構

BC-VCM-LVM-HYPERV 是應用程式與壓縮和解壓縮驅動程式之間的媒介。 壓縮和解壓縮驅動程式會壓縮和解壓縮個別的資料框架。

當應用程式呼叫 BC-VCM-LVM-HYPERV 時，BC-VCM-LVM-HYPERV 會將呼叫轉譯為訊息。 使用 [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) 函式將訊息傳送至適當的壓縮程式或解壓縮程式，以壓縮或解壓縮資料。 BC-VCM-LVM-HYPERV 會接收壓縮或解壓縮驅動程式的傳回值，然後將控制權傳回給應用程式。

如果為訊息定義了宏，宏會展開為 **ICSendMessage** 函式呼叫，為該訊息提供適當的參數。 如果為訊息定義了宏，您的應用程式應該使用它，而不是訊息。 在此總覽中，這些宏會遵循括弧中的訊息。

 

 




