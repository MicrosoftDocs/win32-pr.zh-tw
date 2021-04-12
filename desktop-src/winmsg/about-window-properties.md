---
description: 本總覽討論視窗屬性。
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: 關於視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192825"
---
# <a name="about-window-properties"></a>關於視窗屬性

*視窗屬性* 是指派給視窗的任何資料。 視窗屬性通常是視窗特定資料的控制碼，但它可能是任何值。 每個視窗屬性都是由字串名稱所識別。 有幾個函數可讓應用程式使用視窗屬性。 本總覽將討論下列主題：

-   [使用視窗屬性的優點](#advantages-of-using-window-properties)
-   [指派視窗屬性](#assigning-window-properties)
-   [列舉視窗屬性](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>使用視窗屬性的優點

視窗屬性通常用來將資料與子類別化視窗或多重文件介面中的視窗產生關聯， (MDI) 應用程式。 在任何一種情況下，使用在 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數或類別結構中指定的額外位元組並不方便，原因如下：

-   應用程式可能不知道有多少額外的位元組可用或空間的使用方式。 藉由使用視窗屬性，應用程式可以將資料與視窗建立關聯，而不需要存取額外的位元組。
-   應用程式必須使用位移來存取額外的位元組。 不過，視窗屬性是由其字串識別碼存取，而不是透過位移來存取。

如需子類別化的詳細資訊，請參閱 [windows](about-window-procedures.md)程式子類別化。 如需 MDI 視窗的詳細資訊，請參閱 [多個檔介面](multiple-document-interface.md)。

## <a name="assigning-window-properties"></a>指派視窗屬性

[**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)函式會將視窗屬性和其字串識別碼指派給視窗。 [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)函式會抓取由指定字串識別的視窗屬性。 [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)函式會終結視窗和視窗屬性之間的關聯，但不會摧毀資料本身。 若要終結資料本身，請使用適當的函式來釋放 **RemoveProp** 傳回的控制碼。

## <a name="enumerating-window-properties"></a>列舉視窗屬性

[**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)和 [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)函式會使用應用程式定義的回呼函式來列舉所有視窗的屬性。 如需回呼函數的詳細資訊，請參閱 [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)。

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 包含回呼函式所使用之應用程式定義資料的額外參數。 如需回呼函數的詳細資訊，請參閱 [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa)。

 

 
