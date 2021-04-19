---
description: Microsoft XPS Document Writer (MXDW) 是一種列印到檔的驅動程式，可讓 Windows 應用程式在 windows XP Service Pack 2) SP2 (開始的 Windows 版本上，建立 XML 檔規格 (XPS) 檔檔。
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: 'Microsoft XPS Document Writer (MXDW) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975298"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS Document Writer (MXDW) 

Microsoft XPS Document Writer (MXDW) 是一種列印到檔的驅動程式，可讓 Windows 應用程式在 windows XP Service Pack 2) SP2 (開始的 Windows 版本上，建立 XML 檔規格 (XPS) 檔檔。 使用 MXDW 讓 Windows 應用程式可以將其內容儲存為 XPS 檔，而不需要變更應用程式的任何程式碼。

## <a name="when-to-use"></a>使用時機

如果您想要從 Windows 應用程式建立 XPS 檔，而該檔沒有將其內容儲存為 XPS 檔的選項，您可以選取 [MXDW]。

身為應用程式開發人員，當您的應用程式未提供儲存為 XPS 檔的選項時，建議您 MXDW 想要建立 XPS 檔的使用者。 如需有關 XML 檔規格和 XPS 檔的詳細資訊，請參閱 [XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) 和 [Xps 規格及授權下載](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)。

MXDW 會自動安裝在 windows Vista 和更新版本的 Windows 上，而且可以在 Windows XP SP2 和 Windows Server 2003 上下載和安裝。

## <a name="installation"></a>安裝

在 Windows Vista 和更新版本的 Windows 上，系統會在安裝作業系統時自動安裝 MXDW。

**WINDOWS XP SP2 和 Windows Server 2003**：從 [Microsoft 下載中心](https://www.microsoft.com/downloads/en/default.aspx)下載並安裝 .NET Framework 3.0 或 XPS 基本套件。

## <a name="how-to-use"></a>如何使用

安裝時，MXDW 會在應用程式所顯示的 [列印] 對話方塊中顯示為可用的列印佇列。 將 MXDW 選取為印表機時，系統會提示使用者輸入檔案名，將其建立為可捕獲應用程式列印輸出的 XPS 檔。

下圖顯示在 [Windows Vista 一般列印] 對話方塊中選取為 [印表機] 的 MXDW。

![[列印] 對話方塊的影像，其中顯示 microsoft xps document writer (mxdw 的選取專案) ](images/choosingmxdwinvista.gif)

應用程式開發人員可以使用 [MXDW 設定](mxdw-configuration-settings.md)，自訂 MXDW 的輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[XPS 規格與授權下載](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[isXPS 一致性工具](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[MXDW 設定](mxdw-configuration-settings.md)
</dt> </dl>

 

 
