---
description: Visual Basic Scripting Edition (VBScript) 範例，該範例會使用物件標記來建立憑證註冊控制項物件的實例。
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: 在 VBScript 中具現化的憑證註冊控制項
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da14c55a3c9005f820be8f8d60026bc31ac4920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943491"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a><span data-ttu-id="f0c2f-103">在 VBScript 中具現化的憑證註冊控制項</span><span class="sxs-lookup"><span data-stu-id="f0c2f-103">The Certificate Enrollment Control Instantiated in VBScript</span></span>

<span data-ttu-id="f0c2f-104">下列 Visual Basic Scripting Edition (VBScript) 範例會使用物件標記來建立憑證註冊控制項物件的實例。</span><span class="sxs-lookup"><span data-stu-id="f0c2f-104">The following Visual Basic Scripting Edition (VBScript) example uses the OBJECT tag to create an instance of the Certificate Enrollment Control object.</span></span> <span data-ttu-id="f0c2f-105">當物件超出範圍時，就會從記憶體釋放出來。</span><span class="sxs-lookup"><span data-stu-id="f0c2f-105">The object is freed from memory when it goes out of scope.</span></span>


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<BR>
Certificate Enrollment Control Instantiation Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare a local variable.
Dim varName
' Enable error handling.
On Error Resume Next
' Attempt to use the control, in this case to retrieve a property.
varName = Enroll.MyStoreName
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error!")
    Err.clear
else
    ' The control property was successfully retrieved,
    ' display the property value.
    varName = "MyStoreName is " & varName
    MsgBox( varName )
end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 



