---
description: GINA DLL 的目的是要提供可自訂的使用者識別和驗證程式。 預設 GINA 會藉由將 SAS 事件監視委派給 Winlogon 來執行此工作，以接收和處理 CTL + ALT + DEL 安全的注意順序 (SASs) 。
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: 吉娜
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694152"
---
# <a name="gina"></a><span data-ttu-id="8202f-104">吉娜</span><span class="sxs-lookup"><span data-stu-id="8202f-104">GINA</span></span>

<span data-ttu-id="8202f-105">[*GINA*](/windows/desktop/SecGloss/g-gly)會在 [*Winlogon*](/windows/desktop/SecGloss/w-gly)進程的 [*內容*](/windows/desktop/SecGloss/c-gly)中運作，因此，GINA DLL 在開機過程中會提早載入。</span><span class="sxs-lookup"><span data-stu-id="8202f-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="8202f-106">GINA DLL 必須遵循規則，才能維持系統的完整性（特別是與使用者互動的相關）。</span><span class="sxs-lookup"><span data-stu-id="8202f-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="8202f-107">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="8202f-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="8202f-108">GINA 最常見的用途是與外部裝置（例如智慧卡 [*讀卡機*](/windows/desktop/SecGloss/r-gly)）通訊。</span><span class="sxs-lookup"><span data-stu-id="8202f-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="8202f-109">您必須將設備磁碟機的 start 參數設定為 system (Winnt： SERVICE \_ system \_ start) ，以確保驅動程式是在叫用 GINA 時載入的。</span><span class="sxs-lookup"><span data-stu-id="8202f-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="8202f-110">GINA DLL 的目的是要提供可自訂的使用者識別和驗證程式。</span><span class="sxs-lookup"><span data-stu-id="8202f-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="8202f-111">預設 GINA 會藉由將 SAS 事件監視委派給 Winlogon 來執行此工作，以接收和處理 CTL + ALT + DEL [*安全的注意順序*](/windows/desktop/SecGloss/s-gly) (SASs) 。</span><span class="sxs-lookup"><span data-stu-id="8202f-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="8202f-112">自訂 GINA 會負責將本身設定為接收 SAS 事件 (除了預設的 CTRL + ALT + DEL SAS 事件) 之外，還會在 SAS 事件發生時通知 Winlogon。</span><span class="sxs-lookup"><span data-stu-id="8202f-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="8202f-113">Winlogon 會評估其狀態，以判斷處理自訂 GINA SAS 所需的內容。</span><span class="sxs-lookup"><span data-stu-id="8202f-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="8202f-114">這種處理通常包含對 GINA SAS 處理函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8202f-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="8202f-115">如需特定 GINA 匯出函數的詳細資訊，請參閱 [GINA 匯出](authentication-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="8202f-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="8202f-116">如需使用 GINA 結構傳遞資訊的相關資訊，請參閱 [GINA 結構](authentication-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="8202f-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="8202f-117">主題</span><span class="sxs-lookup"><span data-stu-id="8202f-117">Topic</span></span>                                                                             | <span data-ttu-id="8202f-118">描述</span><span class="sxs-lookup"><span data-stu-id="8202f-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="8202f-119">載入和執行 GINA DLL</span><span class="sxs-lookup"><span data-stu-id="8202f-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="8202f-120">要改變以載入和執行自訂 GINA DLL 的登錄機碼值。</span><span class="sxs-lookup"><span data-stu-id="8202f-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="8202f-121">建立和測試 GINA DLL</span><span class="sxs-lookup"><span data-stu-id="8202f-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="8202f-122">如何測試 GINA DLL。</span><span class="sxs-lookup"><span data-stu-id="8202f-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

