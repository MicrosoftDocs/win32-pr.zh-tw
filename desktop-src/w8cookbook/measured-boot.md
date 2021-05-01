---
title: 測量開機
description: 測量開機
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314339"
---
# <a name="measured-boot"></a><span data-ttu-id="39237-103">測量開機</span><span class="sxs-lookup"><span data-stu-id="39237-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="39237-104">平台</span><span class="sxs-lookup"><span data-stu-id="39237-104">Platforms</span></span>

 <span data-ttu-id="39237-105">**客戶** 端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="39237-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="39237-106">**伺服器** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39237-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="39237-107">Description</span><span class="sxs-lookup"><span data-stu-id="39237-107">Description</span></span>

<span data-ttu-id="39237-108">由於反惡意程式碼 (AM) 軟體在偵測到執行時間惡意程式碼時變得更好且更好，攻擊者也會在建立可隱藏偵測的 rootkit 時變得更好。</span><span class="sxs-lookup"><span data-stu-id="39237-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="39237-109">偵測開機週期初期啟動的惡意程式碼，是大部分的廠商都能處理的挑戰。</span><span class="sxs-lookup"><span data-stu-id="39237-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="39237-110">一般情況下，它們會建立主機作業系統不支援的系統駭客，而且實際上會導致電腦處於不穩定的狀態。</span><span class="sxs-lookup"><span data-stu-id="39237-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="39237-111">到目前為止，Windows 尚未提供良好的方式來偵測並解決這些早期開機的威脅。</span><span class="sxs-lookup"><span data-stu-id="39237-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="39237-112">Windows 8 引進稱為測量開機的新功能，它會測量每個元件，從透過開機啟動驅動程式的固件，將這些測量儲存在電腦上的信賴平臺模組 (TPM) ，然後提供可從遠端測試以驗證用戶端開機狀態的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="39237-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="39237-113">表現</span><span class="sxs-lookup"><span data-stu-id="39237-113">Manifestation</span></span>

<span data-ttu-id="39237-114">測量開機功能提供受信任 (的軟體，可抵禦軟體之前啟動的所有開機元件的詐騙和篡改) 記錄。</span><span class="sxs-lookup"><span data-stu-id="39237-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="39237-115">AM 軟體可以使用記錄來判斷在它是否值得信任之前執行的元件，或是否已受到惡意程式碼感染。</span><span class="sxs-lookup"><span data-stu-id="39237-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="39237-116">本機電腦上的 AM 軟體可以將記錄傳送到遠端伺服器進行評估。</span><span class="sxs-lookup"><span data-stu-id="39237-116">The AM software on the local machine can send the log to a remote server for evaluation.</span></span> <span data-ttu-id="39237-117">遠端伺服器可能會藉由與用戶端上的軟體互動或依適當的頻外機制來啟動補救動作。</span><span class="sxs-lookup"><span data-stu-id="39237-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="39237-118">降低</span><span class="sxs-lookup"><span data-stu-id="39237-118">Mitigation</span></span>

<span data-ttu-id="39237-119">在企業案例中，系統管理員可以控制測量開機資訊的使用方式。</span><span class="sxs-lookup"><span data-stu-id="39237-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="39237-120">在使用者案例中（例如，線上銀行) ），取用者必須選擇將測量開機用於特定的服務。</span><span class="sxs-lookup"><span data-stu-id="39237-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="39237-121">解決方法</span><span class="sxs-lookup"><span data-stu-id="39237-121">Solution</span></span>

<span data-ttu-id="39237-122">正在準備白皮書，以詳細說明必須針對各種測量開機案例進行的 Api 和函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="39237-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




