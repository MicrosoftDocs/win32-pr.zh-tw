---
description: 您可以獨立使用自訂的手勢辨識器，或除了 GestureRecognizer 之外，也可以使用自訂的手勢辨識器。建立自訂的手勢辨識器作為 IStylusSyncPlugin，讓它建立 CustomStylusData，並將外掛程式納入與 GestureRecognizer 相同的 StylusSyncPluginCollection 中。 在 IStylusSyncPlugin 中，將這兩個辨識器的手勢通知合併為應用程式要使用的通知。
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: 使用自訂手勢辨識器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000068"
---
# <a name="using-a-custom-gesture-recognizer"></a>使用自訂手勢辨識器

除了 [**GestureRecognizer**](gesturerecognizer-class.md)之外，您可以單獨使用自訂的手勢辨識器。

將您的自訂手勢辨識器建立為 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)、建立 [CustomStylusData](/previous-versions/ms575208(v=vs.100))，並將外掛程式納入與 [**GestureRecognizer**](gesturerecognizer-class.md)相同的 [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10))中。 在 **IStylusSyncPlugin** 中，將這兩個辨識器的手勢通知合併為應用程式要使用的通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
