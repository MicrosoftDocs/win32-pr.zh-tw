---
title: 列出所有服務連接點的 VB 腳本
ms.assetid: 7a76f872-3e4e-4bb7-8f2d-e30b1246369f
ms.tgt_platform: multiple
description: 深入瞭解： VB 腳本列出所有服務連接點
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1166afff8147785332db615b916fd3ff35c15ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468088"
---
# <a name="vb-script-listing-all-service-connection-points"></a>列出所有服務連接點的 VB 腳本

您可以使用 VB 腳本來管理服務連接點。 下列範例程式碼示範如何列出命令列上所提供之功能變數名稱上的所有服務連接點：


```VB
Option Explicit

Dim scpDN
scpDN = WScript.Arguments.Named("SCP")

If ( scpDN = "" ) Then
    Usage
Else
    ScpProperties scpDN
End If

' End of Main

Sub Usage
    WScript.Echo "USAGE:  ScpProperties /SCP:<SCP DN>"
    WScript.Echo ""
    Wscript.Echo "Remember to put the SCP DN between quotes"
End Sub

Sub ScpProperties( strDN )

    Dim oConn ' As ADODB.Connection
    Set oConn = CreateObject("ADODB.Connection")
    
    oConn.Open "Provider=ADsDSOObject"
    
    Dim oCmd ' As ADODB.Command
    Set oCmd = CreateObject("ADODB.Command")
    oCmd.ActiveConnection = oConn
    
    ' In the next command, the real magic is in knowing LDAP queries
    ' GC means to ask the global catalog.
    oCmd.CommandText = "<GC://" & strDN & ">;" & _
                        "(objectClass=ServiceConnectionPoint);" & _
                        "distinguishedname,name,serviceDNSName," & _
                        "serviceDNSNameType,serviceBindingInformation," & _
                        "serviceClassName,Keywords;" & _
                        "subtree"

    Dim oRs ' As ADODB.Recordset
    Set oRs = oCmd.Execute
    
    Dim lCount ' As Long
    lCount = 0
    Do While (Not oRs.EOF)
    
        Wscript.Echo "SCP Name: " & oRs("name")
        Wscript.Echo "DN: " & oRs("distinguishedname")
        Wscript.Echo "serviceDNSName: " & oRs("serviceDNSName")
        Wscript.Echo "serviceDNSNameType: " & oRs("serviceDNSNameType")
        Wscript.Echo "serviceClassName: " & oRs("serviceClassName")
        Dim a ' As Variant
        Dim l 'As Long
        
        a = oRs("serviceBindingInformation")
        
        If (Not IsNull(a)) Then
            Wscript.Echo "serviceBindingInformation:"
            For l = LBound(a) To UBound(a)
                Wscript.Echo vbTab & a(l)
            Next
            Wscript.Echo 
        End If
        
        a = oRs("Keywords")
        If (Not IsNull(a)) Then
            Wscript.Echo "Keywords: "
            For l = LBound(a) To UBound(a)
                Wscript.Echo vbTab & a(l)
            Next
        End If
        
        oRs.MoveNext
        lCount = lCount + 1
        Wscript.Echo 
    Loop
    
    Wscript.Echo "Total objects = " & lCount
    oConn.Close
    
End Sub
    
```



 

 




