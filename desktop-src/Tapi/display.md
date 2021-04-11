---
description: TAPI 提供手機顯示器的存取權。
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: 顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113192"
---
# <a name="display"></a><span data-ttu-id="72651-103">顯示</span><span class="sxs-lookup"><span data-stu-id="72651-103">Display</span></span>

<span data-ttu-id="72651-104">TAPI 提供電話顯示的存取權。</span><span class="sxs-lookup"><span data-stu-id="72651-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="72651-105">顯示會模型化為具有資料列和資料行的英數位元區域。</span><span class="sxs-lookup"><span data-stu-id="72651-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="72651-106">手機的裝置功能會將電話的顯示大小指定為數據列數目和資料行數目。</span><span class="sxs-lookup"><span data-stu-id="72651-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="72651-107">如果手機裝置沒有顯示，這兩個數字都是零。</span><span class="sxs-lookup"><span data-stu-id="72651-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="72651-108">使用 [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) 將資訊寫入至開啟的電話裝置，並使用 [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) 來取出手機顯示器的目前內容。</span><span class="sxs-lookup"><span data-stu-id="72651-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="72651-109">當手機裝置的顯示變更時，就會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式函式，以通知應用程式狀態變更。</span><span class="sxs-lookup"><span data-stu-id="72651-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="72651-110">此訊息的參數提供了變更的指示。</span><span class="sxs-lookup"><span data-stu-id="72651-110">Parameters to this message provide an indication of the change.</span></span>

 

 



