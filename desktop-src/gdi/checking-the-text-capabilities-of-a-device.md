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
# <a name="checking-the-text-capabilities-of-a-device"></a><span data-ttu-id="d7ec5-103">檢查裝置的文字功能</span><span class="sxs-lookup"><span data-stu-id="d7ec5-103">Checking the Text Capabilities of a Device</span></span>

<span data-ttu-id="d7ec5-104">您可以使用 [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 和 [>enumfontfamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函數來列舉印表機相容記憶體裝置內容中可用的字型。</span><span class="sxs-lookup"><span data-stu-id="d7ec5-104">You can use the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions to enumerate the fonts that are available in a printer-compatible memory device context.</span></span> <span data-ttu-id="d7ec5-105">您也可以使用 [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式來取得裝置文字功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d7ec5-105">You can also use the [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve information about the text capabilities of a device.</span></span> <span data-ttu-id="d7ec5-106">藉由使用 NUMFONTS 索引呼叫 [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) 函式，您可以判斷印表機支援的最小字型數目。</span><span class="sxs-lookup"><span data-stu-id="d7ec5-106">By calling the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function with the NUMFONTS index, you can determine the minimum number of fonts supported by a printer.</span></span> <span data-ttu-id="d7ec5-107"> (個別印表機所支援的字型，可能比使用 NUMFONTS 索引從 **GetDeviceCaps** 傳回值中所指定的字型更多。 ) 使用 TEXTCAPS 索引，您可以識別指定裝置的許多文字功能。</span><span class="sxs-lookup"><span data-stu-id="d7ec5-107">(An individual printer may support more fonts than specified in the return value from **GetDeviceCaps** with the NUMFONTS index.) By using the TEXTCAPS index, you can identify many of the text capabilities of the specified device.</span></span>

 

 
