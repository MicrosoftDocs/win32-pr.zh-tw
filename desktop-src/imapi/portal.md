---
title: 映射主控 API
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103933692"
---
# <a name="image-mastering-api"></a>映射主控 API

## <a name="purpose"></a>目的

Microsoft Windows 映像主控 API 可讓應用程式將映射預備和燒錄至 CD、DVD 和藍光光學儲存體媒體。 以相同方式配置影像的其他類似光碟的媒體也可以使用此 API。

## <a name="developer-audience"></a>開發人員對象

IMAPI.EXE 是針對 C/c + + 和 Visual Basic 開發人員所設計，以及使用 VBScript 撰寫腳本的程式開發人員。

建議您瞭解 CD、DVD 和藍光技術以及檔案系統。 開發人員可能會在 [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go)中熟悉多媒體命令 (MMC) 的最新版本。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Vista 和 Windows Server 2008 開始，原本就支援 IMAPI.EXE 2.0。 啟用 Windows XP 和 Windows Server 2003 的 IMAPI.EXE 2.0 功能需要安裝 [KB932716](https://support.microsoft.com/kb/932716) 更新套件。 如果未安裝此封裝，Windows XP 仍會以原生方式支援 [imapi.exe 1.0](imapiv1.md)。

> [!Note]  
> 適用于儲存體的 Windows Feature Pack 可透過 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)取得。 您可以在 [ [新功能](what-s-new.md) ] 區段中找到有關特定 API 變更的其他資訊。

 

## <a name="in-this-section"></a>本節內容



| 主題                                             | 描述                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [新功能](what-s-new.md)<br/>           | 詳述映射主控 API 每個重要版本的資訊。<br/> |
| [關於 IMAPI.EXE](about-imapi.md)<br/>         | 映射主控 API 的一般資訊。<br/>                         |
| [使用 IMAPI.EXE](using-imapi.md)<br/>         | 工作相關的主題，示範如何使用映射主控 API。<br/>   |
| [IMAPI.EXE 參考](imapi-reference.md)<br/> | IMAPI.EXE 介面和其他程式設計項目的詳細說明。<br/>  |



 

## <a name="additional-resources"></a>其他資源

您可以在下列位置找到有關 IMAPI.EXE 和其他相關主題的進一步資訊：



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft 光學儲存體 Blog](/archive/blogs/opticalstorage/)                | 著重在實際開發案例中，著重于映射主控 API 實作為的主題。                                                                                                                                                                                                                                                 |
| [光學平臺討論論壇](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | 討論 CDROM.SYS、IMAPIv2 和 Live File System 問題。 此論壇著重于系統層級的主題，適用于應用程式開發人員，而非使用者。                                                                                                                                                                                                 |
| [T10 技術委員會](https://www.t10.org/)                       | 國際委員會的資訊技術標準 (INCITS，發音為「深入解析」 ) 。 INCITS 由的認可，並且會在由美國國家標準局 (ANSI) 的核准規則下運作。 這些規則的設計是為了確保自願標準是由產業團隊的共識所開發。 |
| [ (OSTA) 的光學儲存體技術關聯 ](http://www.osta.org/) | 可透過週期性商業化光學儲存體應用程式會議，來塑造產業的未來 (COSA) 、DVD 相容性、行銷、MPV (MusicPhotoVideo) 、UDF 委員會，以及全新的特殊藍色鐳射委員會。 全球有興趣的公司受邀加入組織，並參與其委員會和計畫。               |



 

 

