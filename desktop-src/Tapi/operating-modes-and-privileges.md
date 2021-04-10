---
description: 開啟手機裝置時，應用程式可以要求兩種作業模式的其中一種。
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: 操作模式和許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692236"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="1baca-103">操作模式和許可權</span><span class="sxs-lookup"><span data-stu-id="1baca-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="1baca-104">開啟手機裝置時，應用程式可以要求兩種作業模式的其中一種。</span><span class="sxs-lookup"><span data-stu-id="1baca-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="1baca-105">這些模式反映應用程式要求裝置的許可權：</span><span class="sxs-lookup"><span data-stu-id="1baca-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="1baca-106">開啟監視許可權的電話可讓應用程式判斷電話裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="1baca-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="1baca-107">當偵測到電話裝置上的狀態變更時，會將訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="1baca-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="1baca-108">開啟手機裝置以取得擁有者許可權的應用程式，可以使用可修改電話裝置狀態的作業。</span><span class="sxs-lookup"><span data-stu-id="1baca-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="1baca-109">擁有者許可權也會自動包含完整的監視器許可權。</span><span class="sxs-lookup"><span data-stu-id="1baca-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="1baca-110">在任何時間，指定的電話裝置只能針對擁有者許可權開啟一次，但有多次用於監視許可權。</span><span class="sxs-lookup"><span data-stu-id="1baca-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="1baca-111">所有的 **phoneSet** 作業都需要擁有者許可權，而所有 **phoneGet** 作業只需要監視許可權。</span><span class="sxs-lookup"><span data-stu-id="1baca-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



