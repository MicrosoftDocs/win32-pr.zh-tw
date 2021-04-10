---
title: IMsTscAdvancedSettings KeyBoardLayoutStr 屬性
description: 指定使用中輸入地區設定識別碼的名稱 (先前稱為用於連接的鍵盤配置) 。
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- KeyBoardLayoutStr 屬性遠端桌面服務
- KeyBoardLayoutStr 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，KeyBoardLayoutStr 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685908"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="d9bd3-106">IMsTscAdvancedSettings：： KeyBoardLayoutStr 屬性</span><span class="sxs-lookup"><span data-stu-id="d9bd3-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="d9bd3-107">指定使用中輸入地區設定識別碼的名稱 (先前稱為用於連接的鍵盤配置) 。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="d9bd3-108">如果未設定這個屬性，控制項會使用 [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) 函式所傳回的預設版面配置。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="d9bd3-109">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bd3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9bd3-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="d9bd3-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="d9bd3-111">Property value</span></span>

<span data-ttu-id="d9bd3-112">現用輸入地區設定識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9bd3-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d9bd3-113">Error codes</span></span>

<span data-ttu-id="d9bd3-114">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bd3-115">備註</span><span class="sxs-lookup"><span data-stu-id="d9bd3-115">Remarks</span></span>

<span data-ttu-id="d9bd3-116">屬性是字串形式的八位數十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="d9bd3-117">下方四個數字代表語言識別項，而前四個數字代表該語言內的鍵盤變化。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="d9bd3-118">例如，"00000409" 代表預設的美式英文鍵盤，因為 "0409" 是美國英文的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="d9bd3-119">美式英文鍵盤的 Dvorak 變化具有 "00010409" 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="d9bd3-120">您可以在下列的登錄中找到可用的鍵盤配置（依鍵盤配置識別碼列出）：</span><span class="sxs-lookup"><span data-stu-id="d9bd3-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="d9bd3-121">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bd3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9bd3-122">Requirements</span></span>



| <span data-ttu-id="d9bd3-123">需求</span><span class="sxs-lookup"><span data-stu-id="d9bd3-123">Requirement</span></span> | <span data-ttu-id="d9bd3-124">值</span><span class="sxs-lookup"><span data-stu-id="d9bd3-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bd3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9bd3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bd3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9bd3-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="d9bd3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9bd3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bd3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9bd3-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d9bd3-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d9bd3-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9bd3-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd3-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="d9bd3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bd3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bd3-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd3-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="d9bd3-133">IID</span><span class="sxs-lookup"><span data-stu-id="d9bd3-133">IID</span></span><br/>                      | <span data-ttu-id="d9bd3-134">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="d9bd3-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9bd3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9bd3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bd3-136">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d9bd3-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

