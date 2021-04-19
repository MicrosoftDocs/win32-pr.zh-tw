---
description: 包含 CryptUIDlgSelectCertificate 函數所顯示之對話方塊的相關資訊。
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: CRYPTUI_SELECTCERTIFICATE_STRUCT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985360"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="41bd2-103">CRYPTUI \_ SELECTCERTIFICATE \_ 結構結構</span><span class="sxs-lookup"><span data-stu-id="41bd2-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="41bd2-104">**CRYPTUI \_ SELECTCERTIFICATE \_ 結構** 結構包含 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)函數所顯示之對話方塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="41bd2-105">語法</span><span class="sxs-lookup"><span data-stu-id="41bd2-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="41bd2-106">成員</span><span class="sxs-lookup"><span data-stu-id="41bd2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41bd2-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="41bd2-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-108">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="41bd2-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-109">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="41bd2-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-110">對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="41bd2-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="41bd2-111">如果這個值是 **Null**，父視窗就是預設的桌面視窗。</span><span class="sxs-lookup"><span data-stu-id="41bd2-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="41bd2-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-113">指定 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) 函數的其他選項。</span><span class="sxs-lookup"><span data-stu-id="41bd2-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="41bd2-114">這可以是零或下列值的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="41bd2-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="41bd2-115">值</span><span class="sxs-lookup"><span data-stu-id="41bd2-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="41bd2-116">意義</span><span class="sxs-lookup"><span data-stu-id="41bd2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="41bd2-117"><dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="41bd2-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="41bd2-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="41bd2-119"><dt>**CRYPTUI \_ SELECTCERT \_ 舊版**</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="41bd2-120">指定要顯示舊版對話。</span><span class="sxs-lookup"><span data-stu-id="41bd2-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="41bd2-121"><dt>**CRYPTUI \_ SELECTCERT \_ 多重複選**</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="41bd2-122">允許使用者在對話方塊中選取一個以上的憑證。</span><span class="sxs-lookup"><span data-stu-id="41bd2-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="41bd2-123">如果設定此旗標， [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) 函數一律會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="41bd2-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="41bd2-124">此結構的 **hSelectedCertStore** 成員必須包含憑證存放區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="41bd2-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="41bd2-125">使用者選取的憑證將會新增至此存放區。</span><span class="sxs-lookup"><span data-stu-id="41bd2-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="41bd2-126"><dt>**CRYPTUI \_ SELECTCERT \_ PUT \_ 視窗 \_ 最上層**</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="41bd2-127">強制密碼編譯 UI 成為畫面上的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="41bd2-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="41bd2-128">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="41bd2-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-129">對話方塊的顯示標題。</span><span class="sxs-lookup"><span data-stu-id="41bd2-129">The display title for the dialog box.</span></span> <span data-ttu-id="41bd2-130">如果此成員的值為 **Null**，則會使用 [選取憑證] 的預設標題。</span><span class="sxs-lookup"><span data-stu-id="41bd2-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-131">**dwDontUseColumn**</span><span class="sxs-lookup"><span data-stu-id="41bd2-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-132">可以合併以排除顯示之資料行的旗標。</span><span class="sxs-lookup"><span data-stu-id="41bd2-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="41bd2-133">值</span><span class="sxs-lookup"><span data-stu-id="41bd2-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="41bd2-134">意義</span><span class="sxs-lookup"><span data-stu-id="41bd2-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="41bd2-135"><dt>**CRYPTUI \_選取 \_ ISSUEDTO 資料 \_ 行**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="41bd2-136">不要顯示 **ISSUEDTO** 資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="41bd2-137"><dt>**CRYPTUI \_選取 \_ ISSUEDBY 資料 \_ 行**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="41bd2-138">不要顯示 **ISSUEDBY** 資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="41bd2-139"><dt>**CRYPTUI \_選取 \_ INTENDEDUSE 資料 \_ 行**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="41bd2-140">不要顯示 **IntendedUse** 資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="41bd2-141"><dt>**CRYPTUI \_選取 \_ FRIENDLYNAME 資料 \_ 行**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="41bd2-142">不要顯示名稱資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="41bd2-143"><dt>**CRYPTUI \_選取 \_ 位置資料 \_ 行**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="41bd2-144">不要顯示位置資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="41bd2-145"><dt>**CRYPTUI \_選取 \_ 到期資料 \_ 行**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="41bd2-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="41bd2-146">不要顯示到期資訊。</span><span class="sxs-lookup"><span data-stu-id="41bd2-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="41bd2-147">**szDisplayString**</span><span class="sxs-lookup"><span data-stu-id="41bd2-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-148">對話方塊中顯示的文字，可指示使用者。</span><span class="sxs-lookup"><span data-stu-id="41bd2-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="41bd2-149">如果此成員的值為 **Null**，則會使用預設字串「選取您要使用的憑證」。</span><span class="sxs-lookup"><span data-stu-id="41bd2-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-150">**pFilterCallback**</span><span class="sxs-lookup"><span data-stu-id="41bd2-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-151">[**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc)回呼函式的指標，該函式會篩選對話方塊中顯示的憑證。</span><span class="sxs-lookup"><span data-stu-id="41bd2-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-152">**pDisplayCallback**</span><span class="sxs-lookup"><span data-stu-id="41bd2-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-153">[**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)回呼函式的指標，此函式會顯示使用者選取要查看的憑證。</span><span class="sxs-lookup"><span data-stu-id="41bd2-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-154">**pvCallbackData**</span><span class="sxs-lookup"><span data-stu-id="41bd2-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-155">傳遞給 **pFilterCallback** 和 **pDisplayCallback** 成員所指定之回呼函數的其他資料。</span><span class="sxs-lookup"><span data-stu-id="41bd2-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-156">**cDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="41bd2-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-157">**RghDisplayStores** 陣列中的憑證存放區數目。</span><span class="sxs-lookup"><span data-stu-id="41bd2-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-158">**rghDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="41bd2-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-159">存放區陣列的指標，其中包含可在對話方塊中選取的憑證。</span><span class="sxs-lookup"><span data-stu-id="41bd2-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-160">**cStores**</span><span class="sxs-lookup"><span data-stu-id="41bd2-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-161">**RghStores** 陣列中的憑證存放區數目。</span><span class="sxs-lookup"><span data-stu-id="41bd2-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-162">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="41bd2-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-163">要在建立憑證鏈時搜尋的憑證存放區陣列的指標，並確認對話方塊中顯示的憑證信任。</span><span class="sxs-lookup"><span data-stu-id="41bd2-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-164">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="41bd2-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-165">**RgPropSheetPages** 陣列中的屬性頁數目。</span><span class="sxs-lookup"><span data-stu-id="41bd2-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-166">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="41bd2-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-167">**PROPSHEETPAGE** 結構陣列的指標，代表當選取憑證以供查看時，傳遞給憑證查看對話方塊的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="41bd2-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="41bd2-168">**hSelectedCertStore**</span><span class="sxs-lookup"><span data-stu-id="41bd2-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="41bd2-169">呼叫端所建立之憑證存放區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="41bd2-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="41bd2-170">使用者選取的憑證會新增至此存放區。</span><span class="sxs-lookup"><span data-stu-id="41bd2-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="41bd2-171">如果在呼叫 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)之前和之後，此存放區中的憑證數目是相同的，使用者就會關閉對話方塊，而不選取任何憑證。</span><span class="sxs-lookup"><span data-stu-id="41bd2-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="41bd2-172">如果此結構的 **dwFlags** 成員未包含 **CRYPTUI \_ SELECTCERT \_ 多重** 複選旗標，則不會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="41bd2-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41bd2-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="41bd2-173">Requirements</span></span>



| <span data-ttu-id="41bd2-174">需求</span><span class="sxs-lookup"><span data-stu-id="41bd2-174">Requirement</span></span> | <span data-ttu-id="41bd2-175">值</span><span class="sxs-lookup"><span data-stu-id="41bd2-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41bd2-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41bd2-176">Minimum supported client</span></span><br/> | <span data-ttu-id="41bd2-177">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41bd2-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="41bd2-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41bd2-178">Minimum supported server</span></span><br/> | <span data-ttu-id="41bd2-179">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41bd2-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="41bd2-180">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="41bd2-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41bd2-181">**CRYPTUI \_SELECTCERTIFICATE \_ STRUCTW** (Unicode) 和 **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="41bd2-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41bd2-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41bd2-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41bd2-183">**CryptUIDlgSelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="41bd2-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




