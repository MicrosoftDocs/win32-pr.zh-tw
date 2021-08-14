---
description: 本節討論視窗屬性。 視窗屬性是指派給視窗的任何資料。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: 視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82aba0544e1763d36c0378e5d06dc25d48f3297ba8bc8b3bd8687dbba4b0afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200589"
---
# <a name="window-properties"></a>視窗屬性

視窗屬性是指派給視窗的任何資料。 視窗屬性通常是視窗特定資料的控制碼，但它可能是任何值。 每個視窗屬性都是由字串名稱所識別。

### <a name="in-this-section"></a>本節內容



| Name                                                       | 描述                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [關於視窗屬性](about-window-properties.md)     | 討論視窗屬性。<br/>                                                   |
| [使用視窗屬性](using-window-properties.md)     | 說明如何執行與視窗屬性相關聯的下列工作。<br/> |
| [視窗屬性參考](window-property-reference.md) | 包含 API 參考。<br/>                                                    |



 

### <a name="window-property-functions"></a>視窗屬性函式



| Name                                   | 描述                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | 列舉視窗屬性清單中的所有專案，方法是將它們逐一傳遞給指定的回呼函數。 [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) 會繼續進行，直到列舉最後一個專案或回呼函數傳回 **FALSE** 為止。<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | 列舉視窗屬性清單中的所有專案，方法是將它們逐一傳遞給指定的回呼函數。 [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 會繼續進行，直到列舉最後一個專案或回呼函數傳回 **FALSE** 為止。 <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | 從指定之視窗的屬性清單抓取資料控制碼。 字元字串會識別要取出的控制碼。 字串和控制碼必須已由先前對 [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) 函數的呼叫加入至屬性清單。 <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | 搭配 [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) 函式使用的應用程式定義回呼函數。 函數會從視窗的屬性清單接收屬性專案。 **PROPENUMPROC** 型別定義此回呼函數的指標。 [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca) 是應用程式定義函數名稱的預留位置。 <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | 搭配 [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 函式使用的應用程式定義回呼函數。 函數會從視窗的屬性清單接收屬性專案。 **PROPENUMPROCEX** 型別定義此回呼函數的指標。 [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) 是應用程式定義函數名稱的預留位置。 <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | 從指定之視窗的屬性清單中移除專案。 指定的字元字串會識別要移除的專案。<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | 在指定之視窗的屬性清單中，加入新的專案或變更現有的專案。 如果清單中沒有指定的字元字串，則函式會將新專案加入至清單。 新專案包含字串和控制碼。 否則，函式會將字串的目前控制碼取代為指定的控制碼。 <br/> |



 

 

 
