---
title: 設定 API
description: 提供可讓系統管理員設定、查詢和刪除設定參數的功能。 設定 Api 會使用系統上的 HTTP 伺服器 API 來控制所有應用程式的設定。
ms.assetid: 95a07d41-75c7-43a0-a2cb-707d37de148f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20f1acd5ed610881611028a15b81b5918e4bffcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021389"
---
# <a name="configuration-apis"></a><span data-ttu-id="a8b26-104">設定 API</span><span class="sxs-lookup"><span data-stu-id="a8b26-104">Configuration APIs</span></span>

<span data-ttu-id="a8b26-105">HTTP 伺服器 Api 提供可讓系統管理員設定、查詢和刪除設定參數的功能。</span><span class="sxs-lookup"><span data-stu-id="a8b26-105">The HTTP Server APIs provide functionality for system administrators to set, query and delete configuration parameters.</span></span> <span data-ttu-id="a8b26-106">設定 Api 會使用系統上的 HTTP 伺服器 API 來控制所有應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="a8b26-106">The configuration APIs control the settings for all applications using the HTTP Server API on the system.</span></span>

<span data-ttu-id="a8b26-107">下列各節包含設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a8b26-107">The sections listed below include information about configuration settings.</span></span>

> [!Note]  
> <span data-ttu-id="a8b26-108">這些都是要根據系統和/或應用程式需求套用的選擇性設定步驟。</span><span class="sxs-lookup"><span data-stu-id="a8b26-108">All of these are optional configuration steps to be applied based on system and/or application requirements.</span></span>

 

<span data-ttu-id="a8b26-109">[IP 接聽清單](ip-listen-list.md)  —說明如何設定 HTTP 以在特定的 IP 介面上運作。</span><span class="sxs-lookup"><span data-stu-id="a8b26-109">[IP Listen List](ip-listen-list.md) — describes how to configure HTTP to operate over specific IP interfaces.</span></span>

<span data-ttu-id="a8b26-110">[SSL 憑證](ssl-certificates.md)  —詳述使用 HTTP 伺服器 API 來設定憑證的程式。</span><span class="sxs-lookup"><span data-stu-id="a8b26-110">[SSL Certificates](ssl-certificates.md) — details the procedures to configure certificates with the HTTP Server API.</span></span>

<span data-ttu-id="a8b26-111">[命名空間保留、註冊和路由](namespace-reservations-registrations-and-routing.md)  —概述使用 HTTP 伺服器 API 為電腦上的所有應用程式保留部分命名空間的程式。</span><span class="sxs-lookup"><span data-stu-id="a8b26-111">[Namespace Reservations, Registrations, and Routing](namespace-reservations-registrations-and-routing.md) — outlines the process of reserving portions of the namespace for all applications on the machine using the HTTP Server API.</span></span> <span data-ttu-id="a8b26-112">此外，也會說明註冊和路由要求至特定應用程式的程式。</span><span class="sxs-lookup"><span data-stu-id="a8b26-112">The process to register and route requests to specific applications is also described.</span></span>

<span data-ttu-id="a8b26-113">[HttpCfg.exe](httpcfg-exe.md)  —使用設定 Api 的範例程式。</span><span class="sxs-lookup"><span data-stu-id="a8b26-113">[HttpCfg.exe](httpcfg-exe.md) — a sample program that uses the configuration APIs.</span></span> <span data-ttu-id="a8b26-114">此工具的編譯版本也會隨附在支援工具中的作業系統，以及說明文件的使用說明檔。</span><span class="sxs-lookup"><span data-stu-id="a8b26-114">A compiled version of this tool also ships with the operating system among the support tools, together with a help file that documents how to use it.</span></span>

 

 




