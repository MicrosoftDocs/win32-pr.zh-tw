---
description: 脈衝寬度調整 (PWM) 是產生矩形脈衝波的技術，其會經過調製的脈衝寬度，以產生波形的平均值變化。
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510572"
---
# <a name="pwm-api"></a><span data-ttu-id="d594b-103">PWM API</span><span class="sxs-lookup"><span data-stu-id="d594b-103">PWM API</span></span>

<span data-ttu-id="d594b-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d594b-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d594b-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d594b-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d594b-106">脈衝寬度調整 (PWM) 是產生矩形脈衝波的技術，其會經過調製的脈衝寬度，以產生波形的平均值變化。</span><span class="sxs-lookup"><span data-stu-id="d594b-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="d594b-107">最常見的用法包括驅動的是最高的，也就是降低 Led 或其他相關功能。</span><span class="sxs-lookup"><span data-stu-id="d594b-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="d594b-108">PWM 主要用於物聯網案例。</span><span class="sxs-lookup"><span data-stu-id="d594b-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="d594b-109">關於脈衝寬度調製</span><span class="sxs-lookup"><span data-stu-id="d594b-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="d594b-110">PWM 波形可以依兩個參數分類：</span><span class="sxs-lookup"><span data-stu-id="d594b-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="d594b-111">波形句號 (T) </span><span class="sxs-lookup"><span data-stu-id="d594b-111">A waveform period (T)</span></span>

-   <span data-ttu-id="d594b-112">工作週期，其中波形頻率 (f) 是句號 f = 1/T 之間的倒數</span><span class="sxs-lookup"><span data-stu-id="d594b-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="d594b-113">工作週期描述的是使用 **中** 時間的比例（ / 相對於定期間隔或 **期間**）。</span><span class="sxs-lookup"><span data-stu-id="d594b-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="d594b-114">較低的工作週期會對應到平均低輸出電源，因為大部分的時間都有電源關閉。</span><span class="sxs-lookup"><span data-stu-id="d594b-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="d594b-115">工作週期以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="d594b-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="d594b-116">完全開啟于100%。</span><span class="sxs-lookup"><span data-stu-id="d594b-116">Fully on is 100%.</span></span> <span data-ttu-id="d594b-117">完全關閉是0%。</span><span class="sxs-lookup"><span data-stu-id="d594b-117">Fully off is 0%.</span></span> <span data-ttu-id="d594b-118">使用 **中一半的** 時間是50%。</span><span class="sxs-lookup"><span data-stu-id="d594b-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="d594b-119">想要在 IoT 應用程式中執行 PWM 的開發人員，應該調查 [WINRT PWM 檔。](/uwp/api/windows.devices.pwm)</span><span class="sxs-lookup"><span data-stu-id="d594b-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="d594b-120">脈衝寬度的調製類型</span><span class="sxs-lookup"><span data-stu-id="d594b-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="d594b-121">PWM 會使用 [這些 IO 控制碼](pwm-control-codes.md)、 [結構](pwm-structures.md)和列舉 [。](pwm-enumeration-types.md)</span><span class="sxs-lookup"><span data-stu-id="d594b-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="d594b-122">PWM 也會使用下列函數： [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath)。</span><span class="sxs-lookup"><span data-stu-id="d594b-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 
