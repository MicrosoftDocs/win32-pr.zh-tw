---
description: Windows 通訊端 (Winsock) 服務提供者介面 (SPI) 。
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974716"
---
# <a name="winsock-spi"></a><span data-ttu-id="47c1e-103">Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="47c1e-103">Winsock SPI</span></span>

<span data-ttu-id="47c1e-104">Winsock 服務提供者介面（或 Winsock SPI）是用來建立提供者的特定 Winsock 專業領域;傳輸提供者（例如 TCP/IP 或 IPX/SPX 通訊協定堆疊）使用 Winsock SPI，如同 (DNS) 的命名空間提供者，例如網際網路的網域命名系統。</span><span class="sxs-lookup"><span data-stu-id="47c1e-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="47c1e-105">傳統的網路程式設計，例如讓應用程式透過網路進行通訊，不需要使用 Winsock SPI 介面;請改用標準 [Winsock](winsock-reference.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="47c1e-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="47c1e-106">Winsock SPI 會使用下列函數首碼命名慣例。</span><span class="sxs-lookup"><span data-stu-id="47c1e-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="47c1e-107">前置詞</span><span class="sxs-lookup"><span data-stu-id="47c1e-107">Prefix</span></span> | <span data-ttu-id="47c1e-108">意義</span><span class="sxs-lookup"><span data-stu-id="47c1e-108">Meaning</span></span>                          | <span data-ttu-id="47c1e-109">Description</span><span class="sxs-lookup"><span data-stu-id="47c1e-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="47c1e-110">WSP</span><span class="sxs-lookup"><span data-stu-id="47c1e-110">WSP</span></span>    | <span data-ttu-id="47c1e-111">Windows 通訊端服務提供者</span><span class="sxs-lookup"><span data-stu-id="47c1e-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="47c1e-112">傳輸服務提供者進入點</span><span class="sxs-lookup"><span data-stu-id="47c1e-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="47c1e-113">WPU</span><span class="sxs-lookup"><span data-stu-id="47c1e-113">WPU</span></span>    | <span data-ttu-id="47c1e-114">Windows 通訊端提供者 Upcall</span><span class="sxs-lookup"><span data-stu-id="47c1e-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="47c1e-115">\_服務提供者的 Ws232.dll 進入點</span><span class="sxs-lookup"><span data-stu-id="47c1e-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="47c1e-116">WSC</span><span class="sxs-lookup"><span data-stu-id="47c1e-116">WSC</span></span>    | <span data-ttu-id="47c1e-117">Windows 通訊端設定</span><span class="sxs-lookup"><span data-stu-id="47c1e-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="47c1e-118">WS2 \_ 安裝 applet 的32.dll 進入點</span><span class="sxs-lookup"><span data-stu-id="47c1e-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="47c1e-119">Nsp</span><span class="sxs-lookup"><span data-stu-id="47c1e-119">NSP</span></span>    | <span data-ttu-id="47c1e-120">命名空間提供者</span><span class="sxs-lookup"><span data-stu-id="47c1e-120">Namespace Provider</span></span>               | <span data-ttu-id="47c1e-121">命名空間提供者進入點</span><span class="sxs-lookup"><span data-stu-id="47c1e-121">Namespace provider entry points</span></span>                   |



 

 

 



