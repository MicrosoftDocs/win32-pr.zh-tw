---
description: 您可以使用 EnumFonts 和 >enumfontfamilies 函數來列舉印表機相容記憶體裝置內容中可用的字型。
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: 檢查裝置的文字功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991274"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>檢查裝置的文字功能

您可以使用 [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 和 [>enumfontfamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函數來列舉印表機相容記憶體裝置內容中可用的字型。 您也可以使用 [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式來取得裝置文字功能的相關資訊。 藉由使用 NUMFONTS 索引呼叫 [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) 函式，您可以判斷印表機支援的最小字型數目。  (個別印表機所支援的字型，可能比使用 NUMFONTS 索引從 **GetDeviceCaps** 傳回值中所指定的字型更多。 ) 使用 TEXTCAPS 索引，您可以識別指定裝置的許多文字功能。

 

 
