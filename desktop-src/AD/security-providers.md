---
title: 安全性提供者
description: 安全性支援提供者介面 (SSPI) 支援相互驗證，並且會直接透過 sspi 上的 SSPI Api 和服務（包括 RPC）來公開。
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020828"
---
# <a name="security-providers"></a><span data-ttu-id="a09ce-103">安全性提供者</span><span class="sxs-lookup"><span data-stu-id="a09ce-103">Security Providers</span></span>

<span data-ttu-id="a09ce-104">安全性支援提供者介面 (SSPI) 支援相互驗證，並且會直接透過 sspi 上的 SSPI Api 和服務（包括 RPC）來公開。</span><span class="sxs-lookup"><span data-stu-id="a09ce-104">The Security Support Provider Interface (SSPI) provides support for mutual authentication and is exposed directly through the SSPI APIs and services layered on SSPI, including RPC.</span></span>

<span data-ttu-id="a09ce-105">並非所有可供 SSPI 使用的安全性封裝都支援相互驗證。</span><span class="sxs-lookup"><span data-stu-id="a09ce-105">Not all security packages available to SSPI support mutual authentication.</span></span> <span data-ttu-id="a09ce-106">若要取得相互驗證，應用程式必須要求相互驗證，以及支援的安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="a09ce-106">To obtain mutual authentication, the application must request mutual authentication and a security package that supports it.</span></span> <span data-ttu-id="a09ce-107">例如，在 [具有 SCP 的 Windows 通訊端服務中進行相互驗證](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) 的程式碼範例會使用 windows 2000 隨附的 Secur32.dll 中的 "negotiate" 套件。</span><span class="sxs-lookup"><span data-stu-id="a09ce-107">For example, the code example in [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) uses the "negotiate" package in Secur32.dll, which is included with Windows 2000.</span></span>

 

 




