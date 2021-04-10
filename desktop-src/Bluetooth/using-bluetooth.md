---
title: 使用藍牙
description: 本節說明與針對藍牙撰寫 Windows 應用程式相關的工作。
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684165"
---
# <a name="using-bluetooth"></a><span data-ttu-id="6a3a8-103">使用藍牙</span><span class="sxs-lookup"><span data-stu-id="6a3a8-103">Using Bluetooth</span></span>

<span data-ttu-id="6a3a8-104">本節說明與針對藍牙撰寫 Windows 應用程式相關的工作。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="6a3a8-105">藍牙提供 Ws2bth 和 BluetoothAPIs 檔案中的程式設計定義。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="6a3a8-106">Bthsdpdef .h 檔案必須包含在 BluetoothAPIs 之前。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="6a3a8-107">Ws2bth 必須包含在 Winsock2 之後，才能使用藍牙通訊端。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="6a3a8-108">僅連結至 Bthprops，並避免連結至 Irprops .lib。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="6a3a8-109">Irprops 只是為了回溯相容性而提供。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="6a3a8-110">Bthprops 可在 Windows Vista SDK 中取得。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="6a3a8-111">您可以使用 Windows Vista SDK 來開發 Windows XP Service Pack 2 (SP2) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="6a3a8-112">您可以從 [下載中心](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)取得 WINDOWS Vista SDK。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="6a3a8-113">所有標準同步和重迭的機制，可讓您讀取和寫入目前支援其他位址系列的資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="6a3a8-114">SDK 隨附一些範例程式碼，可顯示使用 Winsock 2.2 和 RFCOMM 通訊協定的簡單藍牙應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="6a3a8-115">您可以在 SDK 安裝位置的 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ 範例 \\ NetDs \\ winsock \\ Bluetooth 中找到範例的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="6a3a8-116">本節將說明下列主題。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-116">This section describes the following topics.</span></span>



| <span data-ttu-id="6a3a8-117">區段</span><span class="sxs-lookup"><span data-stu-id="6a3a8-117">Section</span></span>                                                                                      | <span data-ttu-id="6a3a8-118">Content</span><span class="sxs-lookup"><span data-stu-id="6a3a8-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="6a3a8-119">使用 Windows 通訊端進行藍牙程式設計</span><span class="sxs-lookup"><span data-stu-id="6a3a8-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="6a3a8-120">說明如何使用 Windows 通訊端介面來執行藍牙網路。</span><span class="sxs-lookup"><span data-stu-id="6a3a8-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




