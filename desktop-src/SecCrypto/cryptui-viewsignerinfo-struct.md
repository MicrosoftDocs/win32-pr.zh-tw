---
description: 包含 CryptUIDlgViewSignerInfo 函數的資訊。
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026740"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="d2c63-103">CRYPTUI \_ VIEWSIGNERINFO \_ 結構結構</span><span class="sxs-lookup"><span data-stu-id="d2c63-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="d2c63-104">\[您可以在 [需求] 區段中指定的作業系統中使用 **CRYPTUI \_ VIEWSIGNERINFO \_ 結構** 結構。</span><span class="sxs-lookup"><span data-stu-id="d2c63-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d2c63-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d2c63-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d2c63-106">**CRYPTUI \_ VIEWSIGNERINFO \_ 結構** 結構包含 [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)函數的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2c63-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="d2c63-107">未在已發行的標頭檔中宣告此結構。</span><span class="sxs-lookup"><span data-stu-id="d2c63-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="d2c63-108">若要使用此結構，請使用所示的確切格式來宣告。</span><span class="sxs-lookup"><span data-stu-id="d2c63-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d2c63-109">語法</span><span class="sxs-lookup"><span data-stu-id="d2c63-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="d2c63-110">成員</span><span class="sxs-lookup"><span data-stu-id="d2c63-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2c63-111">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="d2c63-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-112">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d2c63-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-113">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="d2c63-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-114">要作為對話方塊父系的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2c63-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="d2c63-115">如果對話方塊應該沒有父系，這個成員可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d2c63-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d2c63-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-117">一組旗標，可修改 [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) 函式的行為。</span><span class="sxs-lookup"><span data-stu-id="d2c63-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="d2c63-118">目前沒有定義任何旗標，所以此成員必須為零。</span><span class="sxs-lookup"><span data-stu-id="d2c63-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-119">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="d2c63-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-120">以 null 結束的字串指標，其中包含要在對話方塊中顯示的標題。</span><span class="sxs-lookup"><span data-stu-id="d2c63-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="d2c63-121">如果這個成員是 **Null**，則會使用預設標題。</span><span class="sxs-lookup"><span data-stu-id="d2c63-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-122">**pSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="d2c63-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-123">[**CMSG \_ 簽署者 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info)結構的指標，其中包含要顯示的簽署者資訊。</span><span class="sxs-lookup"><span data-stu-id="d2c63-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-124">**hMsg**</span><span class="sxs-lookup"><span data-stu-id="d2c63-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-125">將簽署者資訊解壓縮來源的訊息控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2c63-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-126">**pszOID**</span><span class="sxs-lookup"><span data-stu-id="d2c63-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-127">以 null 結束的 ANSI 字串指標，其中包含 [*物件識別碼*](../secgloss/o-gly.md) 的字串表示 (OID) ，表示應該驗證簽署的憑證。</span><span class="sxs-lookup"><span data-stu-id="d2c63-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="d2c63-128">例如，如果呼叫此方法來查看 [*憑證信任清單*](../secgloss/c-gly.md) 的簽章 (CTL) ，則應該傳入 **szOID 的 \_ KP \_ CTL \_ 使用方式 \_ 簽署** OID 字串。</span><span class="sxs-lookup"><span data-stu-id="d2c63-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="d2c63-129">如果這個成員是 **Null**，則不會驗證憑證的使用方式。</span><span class="sxs-lookup"><span data-stu-id="d2c63-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-130">**>dwreserved**</span><span class="sxs-lookup"><span data-stu-id="d2c63-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-131">目前未使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d2c63-131">This parameter is not currently used.</span></span> <span data-ttu-id="d2c63-132">此成員必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d2c63-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-133">**cStores**</span><span class="sxs-lookup"><span data-stu-id="d2c63-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-134">**RghStores** 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d2c63-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-135">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="d2c63-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-136">**HCERTSTORE** 值的陣列，表示用來搜尋簽署訊息之憑證的其他憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="d2c63-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="d2c63-137">如果這個成員是 **Null**，則不會搜尋其他存放區。</span><span class="sxs-lookup"><span data-stu-id="d2c63-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="d2c63-138">**CStores** 成員包含這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d2c63-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-139">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="d2c63-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-140">**RgPropSheetPages** 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d2c63-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="d2c63-141">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="d2c63-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="d2c63-142">[**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2)結構指標的陣列，可定義要在標準對話方塊中顯示的任何額外頁面。</span><span class="sxs-lookup"><span data-stu-id="d2c63-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="d2c63-143">如果這個成員是 **Null**，則不會顯示任何其他頁面。</span><span class="sxs-lookup"><span data-stu-id="d2c63-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="d2c63-144">**CPropSheetPages** 成員包含這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d2c63-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2c63-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2c63-145">Requirements</span></span>



| <span data-ttu-id="d2c63-146">需求</span><span class="sxs-lookup"><span data-stu-id="d2c63-146">Requirement</span></span> | <span data-ttu-id="d2c63-147">值</span><span class="sxs-lookup"><span data-stu-id="d2c63-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c63-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2c63-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c63-149">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2c63-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d2c63-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2c63-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c63-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2c63-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d2c63-152">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d2c63-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d2c63-153">**CRYPTUI \_VIEWSIGNERINFO \_ STRUCTW** (Unicode) 和 **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d2c63-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2c63-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2c63-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c63-155">**CryptUIDlgViewSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="d2c63-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
