---
title: 'ReadItem 方法 (WSManDisp .h) '
description: 從資源抓取專案，並傳回專案的 XML 表示。
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- ReadItem 方法 Windows 遠端管理
- ReadItem 方法 Windows 遠端管理，列舉值物件
- 列舉值物件 Windows 遠端管理，ReadItem 方法
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024868"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="227d8-106">ReadItem 方法</span><span class="sxs-lookup"><span data-stu-id="227d8-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="227d8-107">從資源抓取專案，並傳回專案的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="227d8-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="227d8-108">語法</span><span class="sxs-lookup"><span data-stu-id="227d8-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="227d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="227d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="227d8-110">*資源*</span><span class="sxs-lookup"><span data-stu-id="227d8-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="227d8-111">專案的 URI。</span><span class="sxs-lookup"><span data-stu-id="227d8-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="227d8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="227d8-112">Return value</span></span>

<span data-ttu-id="227d8-113">專案的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="227d8-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="227d8-114">備註</span><span class="sxs-lookup"><span data-stu-id="227d8-114">Remarks</span></span>

<span data-ttu-id="227d8-115">若要限制讀取的專案數目，請設定 [**Session.BatchItems**](session-batchitems.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="227d8-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="227d8-116">請注意，釋出列舉物件會清除任何暫止的列舉要求。</span><span class="sxs-lookup"><span data-stu-id="227d8-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="227d8-117">[**Session**](session-enumerate.md)方法未取得集合的方式，與 [WMI 查詢](/windows/desktop/WmiSdk/querying-wmi)相同，例如，會傳回 `SELECT * from Win32_LogicalDisk` [**swbemobjectset 搭配使用**](/windows/desktop/WmiSdk/swbemobjectset)中的集合。</span><span class="sxs-lookup"><span data-stu-id="227d8-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="227d8-118">若要將檔案讀取為文字資料流程，您必須建立腳本 [TextStream](/previous-versions//312a5kbt(v=vs.85)) 物件，並呼叫 [TextStream](/previous-versions//h7se9d4f(v=vs.85)) 方法來讀取檔案的每一行。</span><span class="sxs-lookup"><span data-stu-id="227d8-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="227d8-119">以類似的方式，您可以呼叫 **Session。列舉** 方法以取得 [**列舉**](enumerator.md) 值物件，然後呼叫 **ReadItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="227d8-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="227d8-120">如同從文字檔讀取一般，您可以檢查 [**AtEndOfStream**](enumerator-atendofstream.md) 屬性來檢查是否已到達資料項目的結尾。</span><span class="sxs-lookup"><span data-stu-id="227d8-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="227d8-121">範例</span><span class="sxs-lookup"><span data-stu-id="227d8-121">Examples</span></span>

<span data-ttu-id="227d8-122">下列 VBScript 範例會呼叫 [**Session。列舉**](session-enumerate.md) 方法可取得排程工作的清單。</span><span class="sxs-lookup"><span data-stu-id="227d8-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="227d8-123">DisplayOutput 副程式使用 Winrm 命令列工具 XML 轉換檔 (WsmTxt. xsl) 以表格格式輸出資料。</span><span class="sxs-lookup"><span data-stu-id="227d8-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="227d8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="227d8-124">Requirements</span></span>



| <span data-ttu-id="227d8-125">需求</span><span class="sxs-lookup"><span data-stu-id="227d8-125">Requirement</span></span> | <span data-ttu-id="227d8-126">值</span><span class="sxs-lookup"><span data-stu-id="227d8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="227d8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="227d8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="227d8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="227d8-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="227d8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="227d8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="227d8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="227d8-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="227d8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="227d8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="227d8-132"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="227d8-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="227d8-133">Idl</span><span class="sxs-lookup"><span data-stu-id="227d8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="227d8-134"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="227d8-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="227d8-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="227d8-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="227d8-136"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="227d8-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="227d8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="227d8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="227d8-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="227d8-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="227d8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="227d8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="227d8-140">**列舉值**</span><span class="sxs-lookup"><span data-stu-id="227d8-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="227d8-141">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="227d8-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

