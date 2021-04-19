---
title: 使用遠端桌面 ActiveX 控制項
description: 如何使用遠端桌面 ActiveX 控制項自訂遠端桌面服務使用者體驗。
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- 使用遠端桌面 ActiveX 控制項遠端桌面服務遠端桌面服務
- 遠端桌面網頁連線遠端桌面服務，使用
- 遠端桌面通訊協定遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966382"
---
# <a name="using-the-remote-desktop-activex-control"></a>使用遠端桌面 ActiveX 控制項

下列主題包含如何使用遠端桌面 ActiveX 控制項自訂遠端桌面服務使用者體驗的相關資訊。

您可以使用下列格式的遠端桌面 ActiveX 控制項：

-   可編寫腳本的 **控制項**-可執行可安全編寫腳本的介面。 這種形式的控制項可供 web 用戶端或腳本 (（例如 VBScript) 主機）使用。
-   **Nonscriptable 控制項**-提供對腳本而言不安全的額外功能。 這種形式的控制項可以從原生或 managed 程式碼中使用，但這種表單不能由 web 用戶端或僅限腳本的主機使用。

下列清單針對不同的作業系統版本，包含不同控制項的 **CLSID**。 每個 **CLSID** 都與較新的系統版本相容。 例如，Windows Vista 上可編寫腳本的控制項 **CLSID** 將可在較新的系統版本上運作，例如 windows 7。



| 系統版本                          | 可編寫腳本的控制項 CLSID             | Nonscriptable 控制項 CLSID          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1、Windows Server 2012 R2     | 301B94BA-5D25-4A12-BFFE-3B6E7A616585 | 8B918B82-7985-4C24-89DF-C33AD2BBFBCD |
| Windows 8、Windows Server 2012          | 5F681803-2900-4C43-A1CC-CF405404A676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7、Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54D38BF7-B1EF-4479-9674-1BD6EA465258 |
| Windows Vista 包含 Service Pack 1 (SP1) | 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 | 4EB2F086-C818-447E-B32C-C51CE2B30D31 |



 

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[在網頁中內嵌遠端桌面 ActiveX 控制項](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

示範如何使用可編寫腳本之介面的範例。

</dd> <dt>

[使用遠端桌面網頁連線來執行可編寫腳本的虛擬通道](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

示範使用遠端桌面網頁連線執行可編寫腳本之虛擬通道步驟的程式碼範例。

</dd> <dt>

[使用具有虛擬通道的遠端桌面 ActiveX 控制項](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，則可以將此應用程式提供給用戶端電腦使用。

</dd> <dt>

[遠端桌面 ActiveX 控制項隨附的範例網頁](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

遠端桌面網頁連線安裝所在的目錄中 (Default.htm) 的範例網頁。

</dd> <dt>

[提供 RDP 用戶端安全性](providing-for-rdp-client-security.md)
</dt> <dd>

遠端桌面 ActiveX 控制項物件的某些屬性會限制為特定的 Internet Explorer URL 安全性區域。

</dd> <dt>

[停用遠端桌面服務功能](disabling-terminal-services-features.md)
</dt> <dd>

為了加強安全性，您可以選擇停用遠端桌面服務功能。

</dd> </dl>

如需有關安裝遠端桌面 ActiveX 控制項所包含之範例網頁的詳細資訊，請參閱 [遠端桌面 activex 控制項隨附的範例網頁](sample-web-page-included-with-the-remote-desktop-activex-control.md)。

 

 




