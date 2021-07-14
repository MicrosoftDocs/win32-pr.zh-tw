---
title: Windows功能區架構
description: 閱讀 Windows 功能區架構的簡介，這是傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows絲帶
- 功能區
- Windows功能區檔
- 功能區檔
- Windows功能區 API
- 功能區 API
- Windows功能區，架構
- 功能區，架構
- Windows功能區，關於
- 功能區，關於
- Windows功能區、元件
- 功能區、元件
- Windows功能區、視圖
- 功能區、視圖
- Windows功能區，架構
- 功能區，架構
- Windows功能區，Api
- 功能區，Api
- Windows功能區，安全性
- 功能區，安全性
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 98f7dbf42d604f93c76bb9897aa25918d45d126f
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691647"
---
# <a name="windows-ribbon-framework"></a>Windows功能區架構

Windows 功能區架構是一個豐富的命令呈現系統，為傳統 Windows 應用程式的階層式功能表、工具列和工作窗格提供新式替代方法。 類似于 Microsoft Office 2007 Fluent 使用者介面的功能和外觀，功能區架構是由功能區命令列所組成，可透過應用程式視窗頂端的一系列索引標籤來公開應用程式的主要功能，以及內容功能表系統。

## <a name="in-this-section"></a>本節內容



| 主題                                                                           | 描述                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [功能區架構概述](windowsribbon-overviews-entry.md)<br/>      | 本節所包含的主題將探索功能區架構的基本概念。 <br/>                                                                                                                   |
| [功能區架構開發人員指南](windowsribbon-guides-entry.md)<br/>  | 本節所包含的主題將說明 Windows 功能區架構的特定層面。 <br/>                                                                                                          |
| [功能區架構控制項程式庫](windowsribbon-controls-entry.md)<br/> | 本章節包含的主題說明功能區架構所包含的控制項集合。 此處所列的控制項是功能區中公開命令功能的 UI 物件。<br/> |
| [功能區架構參考](windowsribbon-reference-entry.md)<br/>      | 本節所包含的主題會提供功能區架構的參考規格。<br/>                                                                                                       |
| [功能區架構範例](windowsribbon-samples-entry.md)<br/>          | 本節所包含的主題會提供支援 Windows 功能區架構檔的程式碼範例詳細資料。 <br/>                                                                     |
| [功能區架構詞彙](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>開發人員讀者

Windows 功能區架構是設計來供 C/c + + 開發人員和 UI 設計人員使用。

建議的 proficiencies：

- COM 程式設計
- WindowsAPI 程式設計
- XML/XAML 程式設計

建議的基本知識：

- UI 程式設計概念
- 一般 UI 概念

## <a name="minimum-requirements"></a>最低需求



| 需求 | 值 |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端               | Windows 7<br/> Windowsvista Service Pack 2 (SP2) 和[適用于 Windows Vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| 最低支援的伺服器               | Windows Server 2008 R2<br/> Windowsserver 2008 SP2 和[Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| 標頭檔和 IDL 檔案                   | uiribbon .h、uiribbon .idl                                                                                                                                                 |



 

> [!Note]  
> 適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)的 Windows Vista 和 platform update 的[平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)是一組執行時間程式庫，可讓開發人員將 Windows 功能區應用程式的目標設為 Windows Vista 和 Windows 伺服器2008。 所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。 需要適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)或平臺更新的協力廠商應用程式，可以讓 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。

 

## <a name="see-also"></a>另請參閱

[元件物件模型 (COM)](../com/component-object-model--com--portal.md)


[Windows 應用程式開發介面](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

