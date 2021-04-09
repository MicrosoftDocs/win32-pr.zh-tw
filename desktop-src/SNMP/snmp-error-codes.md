---
title: 'SNMP 錯誤碼 (Snmp. h) '
description: Microsoft 會實行 SNMPv2C 規格所定義的下列 SNMP 錯誤碼。
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c1ec7a25490737dd31b2962c09d2e0f36c72d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024698"
---
# <a name="snmp-error-codes"></a><span data-ttu-id="b2abd-103">SNMP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b2abd-103">SNMP Error Codes</span></span>

<span data-ttu-id="b2abd-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b2abd-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2abd-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b2abd-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b2abd-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="b2abd-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b2abd-107">Microsoft 會實行 SNMPv2C 規格所定義的下列 SNMP 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b2abd-107">Microsoft implements the following SNMP error codes that are defined by the SNMPv2C specification.</span></span>



| <span data-ttu-id="b2abd-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="b2abd-108">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="b2abd-109">Description</span><span class="sxs-lookup"><span data-stu-id="b2abd-109">Description</span></span>                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <span data-ttu-id="b2abd-110"><dt>**SNMP \_ERRORSTATUS \_ >aad-userreadusingalternativesecurityid-noerror**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-110"><dt>**SNMP\_ERRORSTATUS\_NOERROR**</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="b2abd-111">代理程式報告傳輸期間未發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2abd-111">The agent reports that no errors occurred during transmission.</span></span><br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <span data-ttu-id="b2abd-112"><dt>**SNMP \_ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-112"><dt>**SNMP\_ERRORSTATUS\_TOOBIG**</dt> <dt>1</dt></span></span> </dl>                                         | <span data-ttu-id="b2abd-113">代理程式無法將要求的 SNMP 操作的結果放在單一 SNMP 訊息中。</span><span class="sxs-lookup"><span data-stu-id="b2abd-113">The agent could not place the results of the requested SNMP operation in a single SNMP message.</span></span><br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <span data-ttu-id="b2abd-114"><dt>**SNMP \_ERRORSTATUS \_ NOSUCHNAME**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-114"><dt>**SNMP\_ERRORSTATUS\_NOSUCHNAME**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="b2abd-115">要求的 SNMP 作業識別未知的變數。</span><span class="sxs-lookup"><span data-stu-id="b2abd-115">The requested SNMP operation identified an unknown variable.</span></span><br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <span data-ttu-id="b2abd-116"><dt>**SNMP \_ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-116"><dt>**SNMP\_ERRORSTATUS\_BADVALUE**</dt> <dt>3</dt></span></span> </dl>                                   | <span data-ttu-id="b2abd-117">要求的 SNMP 操作嘗試變更變數，但卻指定了語法或值錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2abd-117">The requested SNMP operation tried to change a variable but it specified either a syntax or value error.</span></span><br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <span data-ttu-id="b2abd-118"><dt>**SNMP \_ERRORSTATUS \_ READONLY**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-118"><dt>**SNMP\_ERRORSTATUS\_READONLY**</dt> <dt>4</dt></span></span> </dl>                                   | <span data-ttu-id="b2abd-119">要求的 SNMP 操作嘗試根據變數的社區設定檔變更不允許變更的變數。</span><span class="sxs-lookup"><span data-stu-id="b2abd-119">The requested SNMP operation tried to change a variable that was not allowed to change, according to the community profile of the variable.</span></span><br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <span data-ttu-id="b2abd-120"><dt>**SNMP \_ERRORSTATUS \_ GENERR**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-120"><dt>**SNMP\_ERRORSTATUS\_GENERR**</dt> <dt>5</dt></span></span> </dl>                                         | <span data-ttu-id="b2abd-121">在要求的 SNMP 作業期間，此處所列的錯誤除外。</span><span class="sxs-lookup"><span data-stu-id="b2abd-121">An error other than one of those listed here occurred during the requested SNMP operation.</span></span><br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <span data-ttu-id="b2abd-122"><dt>**SNMP \_ERRORSTATUS \_ NOACCESS**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-122"><dt>**SNMP\_ERRORSTATUS\_NOACCESS**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="b2abd-123">無法存取指定的 SNMP 變數。</span><span class="sxs-lookup"><span data-stu-id="b2abd-123">The specified SNMP variable is not accessible.</span></span><br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <span data-ttu-id="b2abd-124"><dt>**SNMP \_ERRORSTATUS \_ WRONGTYPE**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-124"><dt>**SNMP\_ERRORSTATUS\_WRONGTYPE**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="b2abd-125">值指定的類型與變數所需的類型不一致。</span><span class="sxs-lookup"><span data-stu-id="b2abd-125">The value specifies a type that is inconsistent with the type required for the variable.</span></span><br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <span data-ttu-id="b2abd-126"><dt>**SNMP \_ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-126"><dt>**SNMP\_ERRORSTATUS\_WRONGLENGTH**</dt> <dt>8</dt></span></span> </dl>                          | <span data-ttu-id="b2abd-127">值指定的長度與變數所需的長度不一致。</span><span class="sxs-lookup"><span data-stu-id="b2abd-127">The value specifies a length that is inconsistent with the length required for the variable.</span></span><br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <span data-ttu-id="b2abd-128"><dt>**SNMP \_ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-128"><dt>**SNMP\_ERRORSTATUS\_WRONGENCODING**</dt> <dt>9</dt></span></span> </dl>                    | <span data-ttu-id="b2abd-129">值包含抽象語法標記法 (一)  (asn.1) 編碼，與欄位的 asn.1 標記不一致。</span><span class="sxs-lookup"><span data-stu-id="b2abd-129">The value contains an Abstract Syntax Notation One (ASN.1) encoding that is inconsistent with the ASN.1 tag of the field.</span></span><br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <span data-ttu-id="b2abd-130"><dt>**SNMP \_ERRORSTATUS \_ WRONGVALUE**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-130"><dt>**SNMP\_ERRORSTATUS\_WRONGVALUE**</dt> <dt>10</dt></span></span> </dl>                            | <span data-ttu-id="b2abd-131">無法將值指派給變數。</span><span class="sxs-lookup"><span data-stu-id="b2abd-131">The value cannot be assigned to the variable.</span></span><br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <span data-ttu-id="b2abd-132"><dt>**SNMP \_ERRORSTATUS \_ NOCREATION**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-132"><dt>**SNMP\_ERRORSTATUS\_NOCREATION**</dt> <dt>11</dt></span></span> </dl>                            | <span data-ttu-id="b2abd-133">變數不存在，且代理程式無法建立該變數。</span><span class="sxs-lookup"><span data-stu-id="b2abd-133">The variable does not exist, and the agent cannot create it.</span></span><br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <span data-ttu-id="b2abd-134"><dt>**SNMP \_ERRORSTATUS \_ INCONSISTENTVALUE**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-134"><dt>**SNMP\_ERRORSTATUS\_INCONSISTENTVALUE**</dt> <dt>12</dt></span></span> </dl>       | <span data-ttu-id="b2abd-135">值與其他 managed 物件的值不一致。</span><span class="sxs-lookup"><span data-stu-id="b2abd-135">The value is inconsistent with values of other managed objects.</span></span><br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <span data-ttu-id="b2abd-136"><dt>**SNMP \_ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-136"><dt>**SNMP\_ERRORSTATUS\_RESOURCEUNAVAILABLE**</dt> <dt>13</dt></span></span> </dl> | <span data-ttu-id="b2abd-137">將值指派給變數需要配置目前無法使用的資源。</span><span class="sxs-lookup"><span data-stu-id="b2abd-137">Assigning the value to the variable requires allocation of resources that are currently unavailable.</span></span><br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <span data-ttu-id="b2abd-138"><dt>**SNMP \_ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-138"><dt>**SNMP\_ERRORSTATUS\_COMMITFAILED**</dt> <dt>14</dt></span></span> </dl>                      | <span data-ttu-id="b2abd-139">未發生任何驗證錯誤，但未更新任何變數。</span><span class="sxs-lookup"><span data-stu-id="b2abd-139">No validation errors occurred, but no variables were updated.</span></span><br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <span data-ttu-id="b2abd-140"><dt>**SNMP \_ERRORSTATUS \_ UNDOFAILED**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-140"><dt>**SNMP\_ERRORSTATUS\_UNDOFAILED**</dt> <dt>15</dt></span></span> </dl>                            | <span data-ttu-id="b2abd-141">未發生任何驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2abd-141">No validation errors occurred.</span></span> <span data-ttu-id="b2abd-142">有些變數因為無法復原其指派而更新。</span><span class="sxs-lookup"><span data-stu-id="b2abd-142">Some variables were updated because it was not possible to undo their assignment.</span></span><br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <span data-ttu-id="b2abd-143"><dt>**SNMP \_ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-143"><dt>**SNMP\_ERRORSTATUS\_AUTHORIZATIONERROR**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="b2abd-144">發生授權錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2abd-144">An authorization error occurred.</span></span><br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <span data-ttu-id="b2abd-145"><dt>**SNMP \_ERRORSTATUS \_ NOTWRITABLE**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-145"><dt>**SNMP\_ERRORSTATUS\_NOTWRITABLE**</dt> <dt>17</dt></span></span> </dl>                         | <span data-ttu-id="b2abd-146">變數存在，但代理程式無法修改它。</span><span class="sxs-lookup"><span data-stu-id="b2abd-146">The variable exists but the agent cannot modify it.</span></span><br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <span data-ttu-id="b2abd-147"><dt>**SNMP \_ERRORSTATUS \_ INCONSISTENTNAME**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-147"><dt>**SNMP\_ERRORSTATUS\_INCONSISTENTNAME**</dt> <dt>18</dt></span></span> </dl>          | <span data-ttu-id="b2abd-148">變數不存在;因為命名物件實例與其他 managed 物件的值不一致，所以代理程式無法建立該代理程式。</span><span class="sxs-lookup"><span data-stu-id="b2abd-148">The variable does not exist; the agent cannot create it because the named object instance is inconsistent with the values of other managed objects.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b2abd-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2abd-149">Requirements</span></span>



| <span data-ttu-id="b2abd-150">需求</span><span class="sxs-lookup"><span data-stu-id="b2abd-150">Requirement</span></span> | <span data-ttu-id="b2abd-151">值</span><span class="sxs-lookup"><span data-stu-id="b2abd-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b2abd-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2abd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b2abd-153">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2abd-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b2abd-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2abd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b2abd-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2abd-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b2abd-156">標頭</span><span class="sxs-lookup"><span data-stu-id="b2abd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2abd-157"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2abd-157"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2abd-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2abd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2abd-159">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="b2abd-159">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="b2abd-160">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="b2abd-160">SNMP Reference</span></span>](snmp-reference.md)
</dt> </dl>

 

