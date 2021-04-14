---
title: 從 Microsoft 取得物件識別碼
description: 若要成功擴充 Active Directory 架構，您可以從腳本取得根 OID。
ms.assetid: 9ed2dd0a-620d-4856-a8a1-2d2a4468fd4c
ms.tgt_platform: multiple
keywords:
- 從 Microsoft 取得物件識別碼
ms.topic: article
ms.date: 02/19/2021
ms.openlocfilehash: 3daa03798afe8e887e8a33a2fde6bd04ddb5b7cb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514293"
---
# <a name="obtaining-an-object-identifier-from-microsoft"></a><span data-ttu-id="58930-104">從 Microsoft 取得物件識別碼</span><span class="sxs-lookup"><span data-stu-id="58930-104">Obtaining an Object Identifier from Microsoft</span></span>

<span data-ttu-id="58930-105">若要成功擴充 Active Directory 架構，您可以從如下所示的腳本取得根 OID。</span><span class="sxs-lookup"><span data-stu-id="58930-105">To extend the Active Directory schema successfully you can obtain a root OID from a script shown below.</span></span> <span data-ttu-id="58930-106">從腳本產生的 Oid 是唯一的;它們是從唯一的 GUID 對應的。</span><span class="sxs-lookup"><span data-stu-id="58930-106">The OIDs generated from the script are unique; they are mapped from a unique GUID.</span></span> <span data-ttu-id="58930-107">請仔細閱讀最佳做法，因為處理不當的 Oid 可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="58930-107">Please read the best practices carefully as poorly handled OIDs can result in data loss.</span></span>

> [!Note]  
> <span data-ttu-id="58930-108">如需從 Microsoft 取得連結識別碼的指示，請流覽連結的 [屬性](linked-attributes.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="58930-108">For instructions on obtaining a link-Id from Microsoft, please visit the [Linked Attributes](linked-attributes.md) topic.</span></span>

 

## <a name="after-you-have-obtained-a-base-oid"></a><span data-ttu-id="58930-109">取得基底 OID 之後</span><span class="sxs-lookup"><span data-stu-id="58930-109">After You Have Obtained a Base OID</span></span>

<span data-ttu-id="58930-110">當您有基底 OID 之後，請小心決定如何將 Oid 劃分成類別，因為這些 Oid 是包含在前置詞資料表中，而且是 DC 複寫資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="58930-110">Once you have a base OID, be careful when deciding how the OIDs should be divided into categories, because these OIDs are contained in the prefix table and are part of the DC replication data.</span></span> <span data-ttu-id="58930-111">建議您不要建立兩個以上的 OID 類別。</span><span class="sxs-lookup"><span data-stu-id="58930-111">It is recommended that no more than two OID categories be created.</span></span>

<span data-ttu-id="58930-112">您可以為新的架構類別和屬性建立後續 Oid，方法是以 OID 的形式將數位附加至 OID。X，其中 X 可以是您選擇的任何數位。</span><span class="sxs-lookup"><span data-stu-id="58930-112">You can create subsequent OIDs for new schema classes and attributes by appending digits to the OID in the form of OID.X, where X may be any number that you choose.</span></span> <span data-ttu-id="58930-113">一般架構延伸通常會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="58930-113">A common schema extension generally uses the following structure:</span></span>

<span data-ttu-id="58930-114">如果您已1.2.840.113556.1.8000.999999 指派的基底 OID，您可能會建立如下所示的類別。</span><span class="sxs-lookup"><span data-stu-id="58930-114">If your assigned base OID was 1.2.840.113556.1.8000.999999, you might create categories as follows.</span></span>



| <span data-ttu-id="58930-115">OID 基底值</span><span class="sxs-lookup"><span data-stu-id="58930-115">OID base value</span></span>                            | <span data-ttu-id="58930-116">Description</span><span class="sxs-lookup"><span data-stu-id="58930-116">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58930-117">1.2.840.113556.1.8000.999999.1</span><span class="sxs-lookup"><span data-stu-id="58930-117">1.2.840.113556.1.8000.999999.1</span></span><br/> | <span data-ttu-id="58930-118">應用程式類別</span><span class="sxs-lookup"><span data-stu-id="58930-118">Application Classes</span></span><br/> <span data-ttu-id="58930-119">第一個類別會有 OID 1.2.840.113556.1.8000.999999.1.1，第二個類別會有 OID 1.2.840.113556.1.8000.999999.1.2，依此類推。</span><span class="sxs-lookup"><span data-stu-id="58930-119">The first class would have the OID 1.2.840.113556.1.8000.999999.1.1, the second class would have the OID 1.2.840.113556.1.8000.999999.1.2, and so on.</span></span><br/>    |
| <span data-ttu-id="58930-120">1.2.840.113556.1.8000.999999.2</span><span class="sxs-lookup"><span data-stu-id="58930-120">1.2.840.113556.1.8000.999999.2</span></span><br/> | <span data-ttu-id="58930-121">應用程式屬性</span><span class="sxs-lookup"><span data-stu-id="58930-121">Application Attributes</span></span><br/> <span data-ttu-id="58930-122">第一個屬性的 OID 會是1.2.840.113556.1.8000.999999.2.1，第二個屬性的 OID 會是1.2.840.113556.1.8000.999999.2.2，依此類推。</span><span class="sxs-lookup"><span data-stu-id="58930-122">The first attribute's OID would be 1.2.840.113556.1.8000.999999.2.1, the second attribute's OID would be 1.2.840.113556.1.8000.999999.2.2, and so on.</span></span><br/> |

## <a name="script"></a><span data-ttu-id="58930-123">指令碼</span><span class="sxs-lookup"><span data-stu-id="58930-123">Script</span></span>

```shell
' oidgen.vbs 
'  
' THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED  
' OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR  
' FITNESS FOR A PARTICULAR PURPOSE. 
' 
' Copyright (c) Microsoft Corporation. All rights reserved 
' Improvements made by Ryein C. Goddard
' 
' This script is not supported under any Microsoft standard support program or service.  
' The script is provided AS IS without warranty of any kind. Microsoft further disclaims all 
' implied warranties including, without limitation, any implied warranties of merchantability 
' or of fitness for a particular purpose. The entire risk arising out of the use or performance 
' of the scripts and documentation remains with you. In no event shall Microsoft, its authors, 
' or anyone else involved in the creation, production, or delivery of the script be liable for  
' any damages whatsoever (including, without limitation, damages for loss of business profits,  
' business interruption, loss of business information, or other pecuniary loss) arising out of  
' the use of or inability to use the script or documentation, even if Microsoft has been advised  
' of the possibility of such damages. 
' ---------------------------------------------------------------------- 
Function GenerateOID() 
    'Initializing Variables 
    Dim guidString, oidPrefix 
    Dim guidPart0, guidPart1, guidPart2, guidPart3, guidPart4, guidPart5, guidPart6 
    Dim oidPart0, oidPart1, oidPart2, oidPart3, oidPart4, oidPart5, oidPart6 
    On Error Resume Next 
    'Generate GUID 
    Set TypeLib = CreateObject("Scriptlet.TypeLib") 
    guidString = TypeLib.Guid 
    'If no network card is available on the machine then generating GUID can result with an error. 
    If Err.Number <> 0 Then 
        Wscript.Echo "ERROR: Guid could not be generated, please ensure machine has a network card." 
        Err.Clear 
        WScript.Quit 
    End If 
    'Stop Error Resume Next 
    On Error GoTo 0 
    'The Microsoft OID Prefix used for the automated OID Generator 
    oidPrefix = "1.2.840.113556.1.8000.2554" 
    'Split GUID into 6 hexadecimal numbers 
    guidPart0 = Trim(Mid(guidString, 2, 4)) 
    guidPart1 = Trim(Mid(guidString, 6, 4)) 
    guidPart2 = Trim(Mid(guidString, 11, 4)) 
    guidPart3 = Trim(Mid(guidString, 16, 4)) 
    guidPart4 = Trim(Mid(guidString, 21, 4)) 
    guidPart5 = Trim(Mid(guidString, 26, 6)) 
    guidPart6 = Trim(Mid(guidString, 32, 6)) 
    'Convert the hexadecimal to decimal 
    oidPart0 = CLng("&H" & guidPart0) 
    oidPart1 = CLng("&H" & guidPart1) 
    oidPart2 = CLng("&H" & guidPart2) 
    oidPart3 = CLng("&H" & guidPart3) 
    oidPart4 = CLng("&H" & guidPart4) 
    oidPart5 = CLng("&H" & guidPart5) 
    oidPart6 = CLng("&H" & guidPart6) 
    'Concatenate all the generated OIDs together with the assigned Microsoft prefix and return 
    GenerateOID = oidPrefix & "." & oidPart0 & "." & oidPart1 & "." & oidPart2 & "." & oidPart3 & _ 
        "." & oidPart4 & "." & oidPart5 & "." & oidPart6 
End Function 



Set oShell = WScript.CreateObject ("WScript.Shell")
oShell.run "cmd /c Regsvr32 Schmmgmt.dll"

Set objFSO=CreateObject("Scripting.FileSystemObject")
outFile="C:\Users\Administrator\Desktop\oidInfo.txt"
Set objFile = objFSO.CreateTextFile(outFile,True)

'Output the resulted OID with best practice info 
oidText = "Your root OID is: " & VBCRLF & GenerateOID & VBCRLF & VBCRLF & VBCRLF & _ 
    "This prefix should be used to name your schema attributes and classes. For example: " & _ 
    "if your prefix is ""Microsoft"", you should name schema elements like ""microsoft-Employee-ShoeSize"". " & _ 
    "For more information on the prefix, view the Schema Naming Rules in the server " & _  
    "Application Specification (http://www.microsoft.com/windowsserver2003/partners/isvs/appspec.mspx)." & _ 
    VBCRLF & VBCRLF & _ 
    "You can create subsequent OIDs for new schema classes and attributes by appending a .X to the OID where X may " & _ 
    "be any number that you choose.  A common schema extension scheme generally uses the following structure:" & VBCRLF & _ 
    "If your assigned OID was: 1.2.840.113556.1.8000.2554.999999" & VBCRLF & VBCRLF & _ 
    "then classes could be under: 1.2.840.113556.1.8000.2554.999999.1 " & VBCRLF & _  
    "which makes the first class OID: 1.2.840.113556.1.8000.2554.999999.1.1" & VBCRLF & _ 
    "the second class OID: 1.2.840.113556.1.8000.2554.999999.1.2     etc..." & VBCRLF & VBCRLF & _ 
    "Using this example attributes could be under: 1.2.840.113556.1.8000.2554.999999.2 " & VBCRLF & _ 
    "which makes the first attribute OID: 1.2.840.113556.1.8000.2554.999999.2.1 " & VBCRLF & _ 
    "the second attribute OID: 1.2.840.113556.1.8000.2554.999999.2.2     etc..." & VBCRLF & VBCRLF & _ 
     "Here are some other useful links regarding AD schema:" & VBCRLF & _ 
    "Understanding AD Schema" & VBCRLF & _ 
    "http://technet2.microsoft.com/WindowsServer/en/Library/b7b5b74f-e6df-42f6-a928-e52979a512011033.mspx " & _ 
    VBCRLF & VBCRLF & _ 
    "Developer documentation on AD Schema:" & VBCRLF & _ 
    "http://msdn2.microsoft.com/en-us/library/ms675085.aspx " & VBCRLF & VBCRLF & _ 
    "Extending the Schema" & VBCRLF & _ 
    "http://msdn2.microsoft.com/en-us/library/ms676900.aspx " & VBCRLF & VBCRLF & _ 
    "Step-by-Step Guide to Using Active Directory Schema and Display Specifiers " & VBCRLF & _ 
    "http://www.microsoft.com/technet/prodtechnol/windows2000serv/technologies/activedirectory/howto/adschema.mspx " & _ 
    VBCRLF & VBCRLF & _ 
    "Troubleshooting AD Schema " & VBCR & _ 
    "http://technet2.microsoft.com/WindowsServer/en/Library/6008f7bf-80de-4fc0-ae3e-51eda0d7ab651033.mspx  " & _ 
    VBCRLF & VBCRLF 

objFile.Write oidText
objFile.Close

```
