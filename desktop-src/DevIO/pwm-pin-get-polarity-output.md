---
description: 包含要傳回的極性值。
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: 'PWM_PIN_GET_POLARITY_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936241"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="1abe7-103">PWM \_ 針腳 \_ 取得 \_ 極性 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="1abe7-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="1abe7-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1abe7-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1abe7-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1abe7-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1abe7-106">包含要傳回的極性值。</span><span class="sxs-lookup"><span data-stu-id="1abe7-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abe7-107">語法</span><span class="sxs-lookup"><span data-stu-id="1abe7-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="1abe7-108">成員</span><span class="sxs-lookup"><span data-stu-id="1abe7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1abe7-109">**極性**</span><span class="sxs-lookup"><span data-stu-id="1abe7-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="1abe7-110">作為 [**PWM \_ 極性**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) 值的釘選或通道極性。</span><span class="sxs-lookup"><span data-stu-id="1abe7-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="1abe7-111">極性是主動高或主動低。</span><span class="sxs-lookup"><span data-stu-id="1abe7-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1abe7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1abe7-112">Requirements</span></span>



| <span data-ttu-id="1abe7-113">需求</span><span class="sxs-lookup"><span data-stu-id="1abe7-113">Requirement</span></span> | <span data-ttu-id="1abe7-114">值</span><span class="sxs-lookup"><span data-stu-id="1abe7-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1abe7-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1abe7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1abe7-116">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1abe7-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1abe7-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1abe7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1abe7-118">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1abe7-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1abe7-119">最小 KMDF 版本</span><span class="sxs-lookup"><span data-stu-id="1abe7-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="1abe7-120">1.19</span><span class="sxs-lookup"><span data-stu-id="1abe7-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="1abe7-121">最小的 UMDF 版本</span><span class="sxs-lookup"><span data-stu-id="1abe7-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="1abe7-122">2.19</span><span class="sxs-lookup"><span data-stu-id="1abe7-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="1abe7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1abe7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1abe7-124"><dt>Pwm (包含 Pwm) </dt></span><span class="sxs-lookup"><span data-stu-id="1abe7-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1abe7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1abe7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abe7-126">**IOCTL \_ PWM \_ 圖釘 \_ 取得 \_ 極性**</span><span class="sxs-lookup"><span data-stu-id="1abe7-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="1abe7-127">**PWM \_ 極性**</span><span class="sxs-lookup"><span data-stu-id="1abe7-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

