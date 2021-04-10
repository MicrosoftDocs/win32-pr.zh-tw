---
title: 藍牙和 WSAAddressToString
description: WSAAddressToString Windows 通訊端函式是用來將 Bluetooth 裝置位址轉換成字串，然後在抓取裝置服務資訊時，透過 WSAQUERYSET 結構提供給 WSALookupServiceBegin 函式。
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023556"
---
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="e1fab-103">藍牙和 WSAAddressToString</span><span class="sxs-lookup"><span data-stu-id="e1fab-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="e1fab-104">[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows 通訊端函式是用來將 Bluetooth 裝置位址轉換成字串，然後在抓取裝置服務資訊時，透過 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構提供給 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式。</span><span class="sxs-lookup"><span data-stu-id="e1fab-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="e1fab-105">雖然藍牙裝置位址符合20個字元的緩衝區，但 [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) 函式目前會傳回藍牙裝置位址的 **WSAEFAULT** ，除非緩衝區和指定的 *lpdwAddressStringLength* 值設定為40的字元長度。</span><span class="sxs-lookup"><span data-stu-id="e1fab-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="e1fab-106">當 [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)由於緩衝區不足而傳回 **WSAEFAULT** 時，不會使用作業所需的緩衝區大小來更新 *lpdwAddressStringLength* 參數。</span><span class="sxs-lookup"><span data-stu-id="e1fab-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e1fab-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1fab-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1fab-108">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="e1fab-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="e1fab-109">藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="e1fab-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="e1fab-110">藍牙和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="e1fab-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 