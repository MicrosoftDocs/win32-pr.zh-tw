---
description: WIA 提供了一個 TWAIN 相容性層，可讓 TWAIN 感知的應用程式與 Windows 映像取得 (WIA) 裝置進行通訊。
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: TWAIN 相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972426"
---
# <a name="twain-compatibility"></a><span data-ttu-id="64fa4-103">TWAIN 相容性</span><span class="sxs-lookup"><span data-stu-id="64fa4-103">TWAIN Compatibility</span></span>

<span data-ttu-id="64fa4-104">WIA 提供了一個 TWAIN 相容性層，可讓 TWAIN 感知的應用程式與 Windows 映像取得 (WIA) 裝置進行通訊。</span><span class="sxs-lookup"><span data-stu-id="64fa4-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="64fa4-105">TWAIN 感知的應用程式不具有 WIA 功能的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="64fa4-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="64fa4-106">例如，應用程式無法使用 TWAIN 相容性層來隱藏使用者介面。</span><span class="sxs-lookup"><span data-stu-id="64fa4-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="64fa4-107">WIA 裝置會在應用程式中出現兩次，以辨識 WIA 和 TWAIN：一次是透過一般的 WIA 通訊，一次是透過 TWAIN 相容性層。</span><span class="sxs-lookup"><span data-stu-id="64fa4-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="64fa4-108">若要避免列出 WIA 裝置兩次，可感知 WIA 和 TWAIN 的應用程式，都必須篩選出來自 TWAIN 相容性層的 WIA 裝置。</span><span class="sxs-lookup"><span data-stu-id="64fa4-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="64fa4-109">所有通過 TWAIN 相容性層的 WIA 裝置都有 "WIA" 作為前置詞，因此很容易就能進行篩選。</span><span class="sxs-lookup"><span data-stu-id="64fa4-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



