---
description: 單一電話可能會以不同的響鈴模式環形。
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: 環形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944207"
---
# <a name="ring"></a><span data-ttu-id="0bf50-103">環形</span><span class="sxs-lookup"><span data-stu-id="0bf50-103">Ring</span></span>

<span data-ttu-id="0bf50-104">單一電話可能會以不同的響鈴模式環形。</span><span class="sxs-lookup"><span data-stu-id="0bf50-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="0bf50-105">由於有各種不同的環形模式可用，因此環形模式會透過其響鈴模式號碼來識別。</span><span class="sxs-lookup"><span data-stu-id="0bf50-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="0bf50-106">環形模式數位的範圍從零到可用響鈴模式的數目減一。</span><span class="sxs-lookup"><span data-stu-id="0bf50-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="0bf50-107">應用程式用來控制電話裝置環形模式的函式是 [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring)，這會根據指定的響鈴模式來響鈴開啟的電話裝置，並使用 [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring)來傳回已開啟之手機裝置的目前響鈴模式。</span><span class="sxs-lookup"><span data-stu-id="0bf50-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="0bf50-108">當手機裝置的響鈴模式變更時，就會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0bf50-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="0bf50-109">此訊息的參數提供了變更的指示。</span><span class="sxs-lookup"><span data-stu-id="0bf50-109">Parameters to this message provide an indication of the change.</span></span>

 

 



