---
title: 偵測是否已安裝遠端桌面服務角色
description: C \ 程式碼範例，其中顯示如果已安裝並執行遠端桌面服務伺服器角色，則會傳回 True 的方法，否則從 Windows Server 2008 開始會傳回 false。
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f7d094f88271346c97f8d0467b48a266c865d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376260"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>偵測是否已安裝遠端桌面服務角色

您可以使用 [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI 類別來偵測是否已安裝遠端桌面服務伺服器角色。

下列 c # 範例顯示方法，如果遠端桌面服務伺服器角色已安裝且正在執行，則會傳回 **True** ，否則會傳回 **false** 。 由於 [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI 類別只能從 windows Server 2008 開始使用，因此此程式碼與舊版 windows 不相容。


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



 

 