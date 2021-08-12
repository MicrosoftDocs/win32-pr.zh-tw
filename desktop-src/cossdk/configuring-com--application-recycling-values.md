---
description: 您可以使用下列方法來為您的 COM + 應用程式設定應用程式回收值。
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: 設定 COM + 應用程式回收值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2613fb6f063a49d53baa90fad6f7dac862b848c6abf95fddcc36ace25e3d6b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548639"
---
# <a name="configuring-com-application-recycling-values"></a>設定 COM + 應用程式回收值

您可以使用下列方法來為您的 COM + 應用程式設定應用程式回收值。

> [!Note]  
> 您無法回收已設定為以 Windows 服務的方式執行的 com + 應用程式。 此外，程式庫應用程式具有其主機進程的回收和共用屬性。

 

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要設定 COM + 應用程式的應用程式回收，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，以滑鼠右鍵按一下您要回收的 COM + 伺服器應用程式，然後按一下 [ **屬性**]。

2.  在 [共用 **& 回收** ] 索引標籤上，根據您要使用的準則，輸入 **存留期限制 (分鐘** 的值) 、 **記憶體限制 (KB)**、 **到期時間 (分鐘**) 、 **通話限制** 和 **啟用限制**。

    -   **存留期限制** 表示進程在回收之前可執行檔最大分鐘數。 有效範圍是從0到30240分鐘 (21 天) 。 預設分鐘數為0。
    -   **記憶體限制** 表示回收進程之前，進程記憶體使用量的最大數量 (以 kb) 。 如果處理程序的記憶體使用量超出指定的數量達一分鐘以上，就會回收處理程序。 有效範圍是0到 1048576 KB，預設記憶體使用量數量為 0 KB。
    -   **到期時間** 表示在強制關機之前，要等候的分鐘數，以釋放進程中物件的所有外部參考。 有效範圍是從1到1440分鐘 (24 小時) ，而預設到期時間為15分鐘。 只有當已根據其他條件決定將回收處理程序時，才會使用此值。
    -   [**通話限制**] 表示在回收進程之前，應用程式物件可以接受的呼叫數上限。 有效範圍是從0到1048576的呼叫，而預設的呼叫數目為0。
    -   **啟用限制** 表示回收進程之前，要接受的應用程式物件啟用數目上限。 有效範圍是0到1048576的啟用，而啟用的預設數目為0。

    > [!Note]  
    > 如果 **存留期限制**、 **記憶體限制**、 **通話限制** 或 **啟用限制** 值設定為 0 (預設值) ，則會停用該準則的應用程式回收。 當這四個準則都設定為0時，會停用所選應用程式的應用程式回收。

     

3.  按一下 [確定]。

## <a name="visual-basic"></a>Visual Basic

Microsoft Visual Basic 中的下列函式示範如何為您選擇的任何 com + 伺服器應用程式設定應用程式回收值。 若要從 Visual Basic 使用它，請將參考新增至 com + 系統管理員類型程式庫。


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



若要使用函式，請提供應用程式名稱的字串值，以及所需應用程式回收設定的整數值。 下列 Visual Basic 程式碼示範如何將 **RecycleLifetimeLimit** 值設定為5、將 **RecycleMemoryLimit** 值設定為10、將 **RecycleCallLimit** 值設定為9、將 **RecycleActivationLimit** 值設定為100，以及將 **RecycleExpirationTimeout** 值設定為15。


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 應用程式回收概念](com--application-recycling-concepts.md)
</dt> </dl>

 

 



