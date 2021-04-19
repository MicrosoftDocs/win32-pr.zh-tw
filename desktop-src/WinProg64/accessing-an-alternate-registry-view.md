---
title: 存取替代登錄視圖
description: 根據預設，在 WOW64 上執行的 32 位元應用程式會存取 32 位元登錄檢視，而 64 位元應用程式會存取 64 位元登錄檢視。
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- 登錄視圖64位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，登錄視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "106998935"
---
# <a name="accessing-an-alternate-registry-view"></a>存取替代登錄視圖

根據預設，在 WOW64 上執行的 32 位元應用程式會存取 32 位元登錄檢視，而 64 位元應用程式會存取 64 位元登錄檢視。 下列旗標可讓32位應用程式存取64位登錄視圖和64位應用程式中重新導向的金鑰，以存取32位登錄視圖中重新導向的金鑰。 這些旗標對共用的登錄機碼沒有任何影響。 如需詳細資訊，請參閱 [受 WOW64 影響的](shared-registry-keys.md)登錄機碼。



| 旗標名稱         | 值  | 描述                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KEY \_ WOW64 \_ 64KEY | 0x0100 | 從32位或64位應用程式存取64位金鑰。                                                                                                                                                                                   |
| KEY \_ WOW64 \_ 32KEY | 0x0200 | 從32位或64位應用程式存取32位金鑰。<br/>**ARM 上的 Windows 10：** 這是指32位 ARM 進程的32位 ARM 登錄視圖，以及適用于32位 x86 和 64 bit ARM64 進程的32位 x86 登錄視圖。 |



 

您可以在下列登錄函式的 *samDesired* 參數中指定這些旗標：

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

您 \_ \_ 可以指定 key wow64 32KEY 或 key \_ wow64 \_ 64KEY。 如果同時指定這兩個旗標，則函式會失敗，並出現錯誤 \_ \_ 參數無效。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 如果同時指定這兩個旗標，則函式的行為是未定義的。

[**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)函數不能用來存取替代登錄視圖。

以下是從應用程式存取登錄的最佳作法：

-   應用程式使用其中一個旗標存取替代登錄視圖之後，所有後續的作業 (建立、刪除或開啟子登錄機碼) ，必須明確地使用相同的旗標。 否則，可能會發生非預期的行為。
-   若要正確列舉兩個視圖中的所有索引鍵，請在兩個階段中執行列舉。 第一個階段應使用以其中一個旗標開啟的控制碼，而另一個傳遞應使用以其他旗標開啟的控制碼。

> [!Note]  
> **Wow6432Node** 和 **WowAA32Node** 金鑰是保留的。 為了相容，應用程式不應該直接使用這些金鑰。

 

如需透過 WMI 存取替代登錄視圖的詳細資訊，請參閱 [在64位平臺上要求 WMI 資料](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[登錄重新導向程式](registry-redirector.md)
</dt> <dt>

[登錄反映](registry-reflection.md)
</dt> </dl>

 

