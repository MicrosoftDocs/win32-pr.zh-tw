---
description: 為了盡可能簡化驅動程式的執行，Windows 映像取得 (WIA) 提供迷你驅動程式的服務程式庫，可執行 WIA 架構所需的許多系統管理工作。
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: WIA 迷你驅動程式服務程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973073"
---
# <a name="wia-minidriver-service-library"></a><span data-ttu-id="486ba-103">WIA 迷你驅動程式服務程式庫</span><span class="sxs-lookup"><span data-stu-id="486ba-103">WIA Minidriver Service Library</span></span>

<span data-ttu-id="486ba-104">為了盡可能簡化驅動程式的執行，Windows 映像取得 (WIA) 提供迷你驅動程式的服務程式庫，可執行 WIA 架構所需的許多系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="486ba-104">To simplify driver implementation as much as possible, Windows Image Acquisition (WIA) provides a Minidriver Service Library that performs many of the administrative tasks required by the WIA architecture.</span></span> <span data-ttu-id="486ba-105">服務程式庫會提供 helper 函式，以維護裝置的 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="486ba-105">The service library provides helper functions to maintain the device's tree of [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) objects.</span></span>

<span data-ttu-id="486ba-106">基本的服務程式庫函式會執行大部分設備磁碟機都需要執行的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="486ba-106">The basic service library functions perform helper functions that most device drivers would otherwise need to implement.</span></span> <span data-ttu-id="486ba-107">這些函式會讀取和寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="486ba-107">These functions read and write properties.</span></span> <span data-ttu-id="486ba-108">它們也會建立驅動程式專案物件並複製裝置資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="486ba-108">They also create driver item objects and copy device information properties.</span></span>

 

 



