---
title: 偵測是否已安裝遠端桌面服務角色
description: C \ 程式碼範例，示範如果遠端桌面服務伺服器角色已安裝且正在執行，則會傳回 True 的方法，否則從 Windows server 2008 開始，則為 false。
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf7ac1932c32ea797783d04f4e279bab03339c9b7620c11e72d4b755f084736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871758"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>偵測是否已安裝遠端桌面服務角色

您可以使用 [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI 類別來偵測是否已安裝遠端桌面服務伺服器角色。

下列 c # 範例顯示方法，如果遠端桌面服務伺服器角色已安裝且正在執行，則會傳回 **True** ，否則會傳回 **false** 。 由於 [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI 類別只能從 Windows Server 2008 開始提供，因此此程式碼與舊版 Windows 不相容。


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 