---
title: 開啟和關閉混音器裝置
description: 開啟和關閉混音器裝置
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- 多媒體音訊，開啟混音器裝置
- 音訊，開啟混音器裝置
- 音訊 mixers，開啟
- mixers，開啟
- 多媒體音訊，關閉混音器裝置
- 音訊，關閉混音器裝置
- 音訊 mixers，關閉
- mixers，關閉
- 開啟混音器裝置
- 關閉混音器裝置
- 裝置識別碼和裝置控制碼
- 音訊 mixers、裝置識別碼和裝置控制碼
- mixers、裝置識別碼和裝置控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023324"
---
# <a name="opening-and-closing-mixer-devices"></a>開啟和關閉混音器裝置

當您想要使用混音器裝置時，您可以直接使用它，也可以先明確開啟裝置，再使用它。 明確開啟混音器裝置可提供兩個主要優點：

-   它可保證該混音器裝置持續存在。
-   它可讓您接收音訊行和控制項變更的通知。

您可以使用 [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) 函式來明確開啟混音器裝置。 此函式會採用裝置識別碼的參數、記憶體位置的指標，以及每種裝置類型獨有的其他值。 記憶體位置會以裝置控制碼填滿。 呼叫其他音訊混音器函式時，請使用此裝置控制碼來識別開啟混音器裝置。 只要混音器裝置的控制碼存在，裝置就會繼續存在於系統中。 如果混音器裝置發生設定變更，但未明確開啟，則您的應用程式可能突然無法存取它。

> [!Note]  
> 裝置識別碼和裝置控制碼之間的差異很重要。 當您使用 **mixerOpen** 開啟設備磁碟機時，會傳回裝置控制碼。 裝置識別碼是由系統中的裝置數目隱含決定;您可以使用 [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) 函式來取得這個數位。

 

您可以使用 [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) 函式來關閉混音器裝置。 使用完畢後，您應該關閉裝置。

 

 