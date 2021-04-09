---
description: Comm/datamodem/portname 裝置類別是由數據機所連接的裝置名稱所組成。
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: 通訊/datamodem/portname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850804"
---
# <a name="commdatamodemportname"></a><span data-ttu-id="39234-103">通訊/datamodem/portname</span><span class="sxs-lookup"><span data-stu-id="39234-103">comm/datamodem/portname</span></span>

<span data-ttu-id="39234-104">Comm/datamodem/portname 裝置類別是由數據機所連接的裝置名稱所組成。</span><span class="sxs-lookup"><span data-stu-id="39234-104">The comm/datamodem/portname device class consists of the device names to which modems are attached.</span></span> <span data-ttu-id="39234-105">在對 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 函式的呼叫中指定這個裝置名稱時，函式會以以 null 終止的 ANSI (非 Unicode) 字串來填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) 結構，指定連接指定數據機的埠名稱，例如 "COM1 \\ 0"。</span><span class="sxs-lookup"><span data-stu-id="39234-105">When this device name is specified in a call to the [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function, the function fills the [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure with a null-terminated ANSI (not Unicode) string specifying the name of the port to which the specified modem is attached, such as "COM1\\0".</span></span> <span data-ttu-id="39234-106">這主要是為了在使用者介面中進行識別，但在某些情況下，如果服務提供者尚未讓裝置開啟) ，就可以在某些情況下用來直接開啟裝置，略過服務提供者的 (。</span><span class="sxs-lookup"><span data-stu-id="39234-106">This is intended primarily for identification purposes in the user interface, but could be used under some circumstances to open the device directly, bypassing the service provider (if the service provider does not already have the device open itself).</span></span> <span data-ttu-id="39234-107">如果沒有與裝置相關聯的通訊埠，就 \\ 會在 **VARSTRING** 結構中傳回 null 字串 ( "0" )  (字串長度為 1) 。</span><span class="sxs-lookup"><span data-stu-id="39234-107">If there is no port associated with the device, a null string ("\\0") is returned in the **VARSTRING** structure (with a string length of 1).</span></span>

 

 



