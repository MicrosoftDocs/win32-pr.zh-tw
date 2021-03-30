---
description: 示範如何使用 Shell \_ NotifyIcon 和 shell \_ NotifyIconGetRect api 來顯示通知圖示。
title: NotificationIcon 範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973289"
---
# <a name="notificationicon-sample"></a>NotificationIcon 範例

示範如何使用 [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 和 [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) api 來顯示通知圖示。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="description"></a>Description

除了使用 [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 和 [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) 來顯示通知圖示之外，此範例也會示範如何顯示豐富的飛出視窗、操作功能表和批註提示。

> [!Note]  
> [**Shell \_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) 僅適用于 Windows 7 和更新版本。

 

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [NotificationIcon 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **NotificationIcon** 專案目錄。
2.  輸入 `msbuild NotificationIcon.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **NotificationIcon** 專案目錄。
2.  按兩下 NotificationIcon .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `NotificationIcon.exe` 。 或者，從 Windows 檔案總管按兩下 NotificationIcon.exe 的圖示。

> [!Note]  
> 以 GUID 指定的通知圖示會藉由驗證只有單一應用程式註冊來防止詐騙。 這項註冊會在您第一次呼叫 Shell NotifyIcon 時執行 \_ (NIM \_ ADD，... ) ，而且會儲存呼叫應用程式的完整路徑名稱。 如果您稍後將二進位檔案移至不同的位置，系統將不會允許重新加入該圖示。 如需詳細資訊，請參閱 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 。

 

 

 



