---
title: 'WSMan 物件 (WSManDisp .h) '
description: 提供用來建立會話的方法和屬性，以會話物件表示。
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- WSMan 物件 Windows 遠端管理
- WSMan 物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384002"
---
# <a name="wsman-object"></a><span data-ttu-id="3ac1e-105">WSMan 物件</span><span class="sxs-lookup"><span data-stu-id="3ac1e-105">WSMan object</span></span>

<span data-ttu-id="3ac1e-106">提供用來建立會話的方法和屬性，以 [**會話**](session.md) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="3ac1e-107">任何 Windows 遠端管理作業都需要建立連接至遠端電腦、[*基礎管理控制器*](windows-remote-management-glossary.md) (BMC) 或本機電腦的 [**會話**](session.md)。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="3ac1e-108">作業包括取得、寫入、列舉資料或叫用方法。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="3ac1e-109">成員</span><span class="sxs-lookup"><span data-stu-id="3ac1e-109">Members</span></span>

<span data-ttu-id="3ac1e-110">**WSMan** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ac1e-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="3ac1e-111">方法</span><span class="sxs-lookup"><span data-stu-id="3ac1e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ac1e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3ac1e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ac1e-113">方法</span><span class="sxs-lookup"><span data-stu-id="3ac1e-113">Methods</span></span>

<span data-ttu-id="3ac1e-114">**WSMan** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3ac1e-115">方法</span><span class="sxs-lookup"><span data-stu-id="3ac1e-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3ac1e-116">描述</span><span class="sxs-lookup"><span data-stu-id="3ac1e-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-118">建立 <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> 物件，這個物件會指定建立遠端會話時使用的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-120">建立可指定的 <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> 物件：</span><span class="sxs-lookup"><span data-stu-id="3ac1e-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="3ac1e-121"><a href="windows-remote-management-glossary.md"><em>資源</em></a>的完整路徑或單一資料片段。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="3ac1e-122">特定資源實例的 <a href="windows-remote-management-glossary.md"><em>選取器</em></a> 。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="3ac1e-123">提供其他資料給資源提供者的 <a href="windows-remote-management-glossary.md"><em>選項</em></a> 。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-125">建立可用於後續網路作業的 <a href="session.md"><strong>會話</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-127">傳回列舉旗標<strong>EnumerationFlagHierarchyDeep</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-129">傳回列舉旗標<strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-131">傳回列舉旗標<strong>EnumerationFlagHierarchyShallow</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-133">傳回列舉常數 <strong>WSManFlagNonXmlText</strong> 的值，以用於 Session 的 <em>Flags</em> 參數。 <a href="session-enumerate.md"><strong>列舉</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-135">傳回列舉旗標<strong>EnumerationFlagReturnEPR</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-137">傳回列舉旗標<strong>EnumerationFlagReturnObject</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-139">傳回列舉旗標<strong>EnumerationFlagReturnObjectAndEPR</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-140"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-141">傳回格式化的字串，其中包含錯誤號碼的文字。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-143">傳回驗證旗標<strong>WSManFlagCredUsernamePassword</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-145">傳回驗證旗標<strong>WSManFlagEnableSPNServerPort</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-147">傳回驗證旗標<strong>WSManFlagNoEncryption</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-149">傳回<strong>WSManFlagSkipCACheck</strong> authentication 旗標的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-151">傳回驗證旗標<strong>WSManFlagSkipCNCheck</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-153">傳回驗證旗標<strong>WSManFlagUseBasic</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-155">傳回驗證旗標<strong>WSManFlagUseDigest</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-157">傳回驗證旗標<strong>WSManFlagUseKerberos</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-159">傳回驗證旗標<strong>WSManFlagUseNegotiate</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3ac1e-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-161">傳回驗證旗標<strong>WSManFlagUseNoAuthentication</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3ac1e-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ac1e-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3ac1e-163">傳回驗證旗標<strong>WSManFlagUTF8</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="3ac1e-164">屬性</span><span class="sxs-lookup"><span data-stu-id="3ac1e-164">Properties</span></span>

<span data-ttu-id="3ac1e-165">**WSMan** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="3ac1e-166">屬性</span><span class="sxs-lookup"><span data-stu-id="3ac1e-166">Property</span></span>                                            | <span data-ttu-id="3ac1e-167">存取類型</span><span class="sxs-lookup"><span data-stu-id="3ac1e-167">Access type</span></span>          | <span data-ttu-id="3ac1e-168">Description</span><span class="sxs-lookup"><span data-stu-id="3ac1e-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="3ac1e-169">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="3ac1e-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="3ac1e-170">唯讀</span><span class="sxs-lookup"><span data-stu-id="3ac1e-170">Read-only</span></span><br/> | <span data-ttu-id="3ac1e-171">取得目前裝載進程未處理的命令列。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="3ac1e-172">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="3ac1e-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="3ac1e-173">唯讀</span><span class="sxs-lookup"><span data-stu-id="3ac1e-173">Read-only</span></span><br/> | <span data-ttu-id="3ac1e-174">取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="3ac1e-175">備註</span><span class="sxs-lookup"><span data-stu-id="3ac1e-175">Remarks</span></span>

<span data-ttu-id="3ac1e-176">**WSMan** 物件會對應至 [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)和 [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)介面。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="3ac1e-177">**WSMan** 是唯一可以使用 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))直接建立的物件。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="3ac1e-178">範例</span><span class="sxs-lookup"><span data-stu-id="3ac1e-178">Examples</span></span>

<span data-ttu-id="3ac1e-179">下列程式碼範例示範如何將 **WSMan** 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="3ac1e-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="3ac1e-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ac1e-180">Requirements</span></span>



| <span data-ttu-id="3ac1e-181">需求</span><span class="sxs-lookup"><span data-stu-id="3ac1e-181">Requirement</span></span> | <span data-ttu-id="3ac1e-182">值</span><span class="sxs-lookup"><span data-stu-id="3ac1e-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac1e-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ac1e-183">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac1e-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ac1e-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3ac1e-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ac1e-185">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac1e-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ac1e-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3ac1e-187">標頭</span><span class="sxs-lookup"><span data-stu-id="3ac1e-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac1e-188"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac1e-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ac1e-189">Idl</span><span class="sxs-lookup"><span data-stu-id="3ac1e-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ac1e-190"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ac1e-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ac1e-191">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ac1e-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ac1e-192"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ac1e-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ac1e-193">DLL</span><span class="sxs-lookup"><span data-stu-id="3ac1e-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ac1e-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ac1e-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ac1e-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ac1e-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac1e-196">WinRM 腳本 API</span><span class="sxs-lookup"><span data-stu-id="3ac1e-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="3ac1e-197">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="3ac1e-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3ac1e-198">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="3ac1e-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3ac1e-199">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="3ac1e-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3ac1e-200">從本機電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="3ac1e-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="3ac1e-201">從遠端電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="3ac1e-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

