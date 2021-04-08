---
description: 本主題說明如何呈現要列印的程式資料。
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 如何：轉譯列印工作資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852416"
---
# <a name="how-to-render-print-job-data"></a>如何：轉譯列印工作資料

本主題說明如何呈現要列印的程式資料。 本主題不會詳細說明如何呈現特定圖形或文字影像。 相反地，它會說明如何管理程式資料，並將其轉譯為 XPS 檔，以使用 [Xps 列印 API](xps-printing.md)傳送至印表機。

## <a name="overview"></a>概觀

轉譯列印工作資料以進行列印時，需要取得程式專屬的資料，例如文字、影像和格式，以及將其轉換成與目的地印表機相容的格式。 將資料傳送至印表機的程式必須以印表機驅動程式所需的格式來傳送。

使用 [Xps 列印 API](xps-printing.md) 將資料傳送至印表機，而且需要將資料格式化為 XPS 檔。 若要產生 XPS 列印 API 所需的 XPS 檔內容，範例程式會使用 [Xps 檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85))。

如果程式內容的格式與印表機不相容，則必須在將其傳送至印表機之前先轉譯。 如果程式使用 [XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85)) 來管理其程式內容，則程式內容會採用可直接傳送到 [XPS 列印 API](xps-printing.md) 的格式，而且在您將它傳送至印表機之前，不需要任何額外的轉譯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS 列印 API](xps-printing.md)
</dt> </dl>

 

 
