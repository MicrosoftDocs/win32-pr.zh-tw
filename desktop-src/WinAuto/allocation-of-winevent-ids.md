---
title: 配置 New-winevent 識別碼
description: 每個 New-winevent 僅供特定用途使用。 針對非預期的目的使用 New-winevent 可能會導致與其他應用程式或作業系統發生衝突，而導致應用程式或作業系統變得不穩定。
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e877c6adcba79870d887e0bdb0d2eb9137d9e04fda4c1cc770414d0dd01f96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326880"
---
# <a name="allocation-of-winevent-ids"></a>配置 New-winevent 識別碼

每個 New-winevent 僅供特定用途使用。 針對非預期的目的使用 New-winevent 可能會導致與其他應用程式或作業系統發生衝突，而導致應用程式或作業系統變得不穩定。

Microsoft 定義了數種不同的 WinEvents 類別，每個類別目錄都定義了一或多個範圍的值，以做為 New-winevent 識別碼使用。 Community 保留範圍 (0xA000-0xAFFF) 適用于需要定義新 WinEvents 的應用程式。 使用來自此範圍的值有助於降低衝突的風險;不過，建立新 WinEvents 的開發人員仍然需要共同作業，以避免應用程式之間發生衝突。

下表顯示 New-winevent 類別目錄，以及針對每個類別目錄定義的值範圍。



| 類別                                                | 範圍         | 目前使用中 | 註解                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Microsoft Active Accessibility (系統保留) 的事件 | 0x0001-0x00FF | 0x0001-0x0020    | 事件 \_ 系統 \_ \* 事件識別碼                                                                     |
| Microsoft Active Accessibility (系統保留) 的事件 | 0x4001-0x40FF | 0x4001-0x4007    | 事件 \_ 主控台 \_ \* 事件識別碼                                                                    |
| 消費者介面自動化 (系統保留) 的事件                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | 消費者介面自動化事件識別碼                                                                         |
| 消費者介面自動化 (系統保留) 的事件                  | 0x7500-0x75FF | 0x7530-0x759B    | 消費者介面自動化屬性變更的事件識別碼                                                        |
| Microsoft Active Accessibility (系統保留) 的事件 | 0x8000-0x80FF | 0x8000-0x8015    | 事件 \_ 物件 \_ \* 事件識別碼                                                                     |
| OEM 保留                                            | 0x0101-0x01FF | 0x0101-0x0122    | IAccessible2 事件識別碼                                                                          |
| Community保留                                      | 0xA000-0xAFFF | 無             | 針對協助工具互通性同盟所定義的新事件保留 (AIA) 規格 |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | 保留給在執行時間配置的自訂事件                                                 |



 

下列主題會更詳細地描述 New-winevent 範圍。

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Microsoft Active Accessibility 和消費者介面自動化事件

New-winevent 識別碼的五個範圍保留供 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化使用。 第一個範圍 (0x0001-0x00FF) 保留給系統層級的事件，通常用來描述影響系統中所有應用程式的情況。 第二個範圍 (0x4001-0x40FF) 保留給 Windows 主控台特定事件。 第三個 (0x4E00-0x4EFF) 和第四個範圍 (0x7500）-0x75FF) 用於反映消費者介面自動化事件。 最後，第五個範圍 (0x8000： 0x80FF) 適用于與某個應用程式內物件相關的情況的物件層級事件。

所有 Microsoft Active Accessibility 和消費者介面自動化事件都定義于 WinUser .h 和 Uiautomationclient.dll. h 標頭檔中。

## <a name="oem-reserved-events"></a>OEM 保留的事件

OEM 保留範圍開放給任何需要使用 WinEvents 做為通訊機制的人。 開發人員應定義和發佈事件定義以及其參數 (或也可以使用相關聯的物件類型) 以進行事件處理，以便避免事件識別碼意外發生衝突。 IAccessible2 規格會使用 OEM 保留範圍的一部分。

## <a name="community-reserved-events"></a>Community保留的事件

Community 保留範圍適用于協助工具互通性聯盟 (AIA) 所指定的 WinEvents，可用於整個產業。 強烈建議您使用此範圍內的值來定義及發佈官方規格。

## <a name="atom-events"></a>ATOM 事件

ATOM 範圍是保留給在執行時間透過消費者介面自動化擴充性 API 所配置的事件識別碼。 請勿將 ATOM 範圍中的值用於任何其他用途。 從 ATOM 範圍配置 WinEvents 的建議方法是使用 [**GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) 函數搭配字串 GUID。

## <a name="using-values-from-a-reserved-range"></a>使用保留範圍內的值

根據 New-winevent 規格，無法使用系統保留範圍中的值或任何其他未定義的範圍，而不需要修改 SDK。 針對新的 WinEvents，應用程式應該使用 OEM 保留或 Community 保留範圍中的值。 在使用新的 New-winevent 之前，強烈建議開發人員以公開且廣泛的方式共用其規格，而且應該使用協助工具互通性聯盟來定義 New-winevent 規格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[協助工具互通性聯盟](https://www.atia.org/)
</dt> </dl>

 

 