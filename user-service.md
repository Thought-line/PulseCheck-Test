// KAN-9 Refactor user service module
// Split the user service into profile, auth and settings helpers.

const db = require('./db');

/**
 * Get the user's name.
 */
async function getUserName(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.name;
}

/**
 * Update the user's name.
 */
async function updateUserName(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('name is required');
  }
  await db.users.update(userId, { name: value, updatedAt: new Date() });
  return getUserName(userId);
}

/**
 * Get the user's email.
 */
async function getUserEmail(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.email;
}

/**
 * Update the user's email.
 */
async function updateUserEmail(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('email is required');
  }
  await db.users.update(userId, { email: value, updatedAt: new Date() });
  return getUserEmail(userId);
}
/**
 * Get the user's phone.
 */
async function getUserPhone(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.phone;
}

/**
 * Update the user's phone.
 */
async function updateUserPhone(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('phone is required');
  }
  await db.users.update(userId, { phone: value, updatedAt: new Date() });
  return getUserPhone(userId);
}

/**
 * Get the user's address.
 */
async function getUserAddress(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.address;
}

/**
 * Update the user's address.
 */
async function updateUserAddress(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('address is required');
  }
  await db.users.update(userId, { address: value, updatedAt: new Date() });
  return getUserAddress(userId);
}

/**
 * Get the user's city.
 */
async function getUserCity(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.city;
}

/**
 * Update the user's city.
 */
async function updateUserCity(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('city is required');
  }
  await db.users.update(userId, { city: value, updatedAt: new Date() });
  return getUserCity(userId);
}

/**
 * Get the user's country.
 */
async function getUserCountry(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.country;
}

/**
 * Update the user's country.
 */
async function updateUserCountry(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('country is required');
  }
  await db.users.update(userId, { country: value, updatedAt: new Date() });
  return getUserCountry(userId);
}

/**
 * Get the user's avatar.
 */
async function getUserAvatar(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.avatar;
}

/**
 * Update the user's avatar.
 */
async function updateUserAvatar(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('avatar is required');
  }
  await db.users.update(userId, { avatar: value, updatedAt: new Date() });
  return getUserAvatar(userId);
}

/**
 * Get the user's bio.
 */
async function getUserBio(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.bio;
}

/**
 * Update the user's bio.
 */
async function updateUserBio(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('bio is required');
  }
  await db.users.update(userId, { bio: value, updatedAt: new Date() });
  return getUserBio(userId);
}

/**
 * Get the user's language.
 */
async function getUserLanguage(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.language;
}

/**
 * Update the user's language.
 */
async function updateUserLanguage(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('language is required');
  }
  await db.users.update(userId, { language: value, updatedAt: new Date() });
  return getUserLanguage(userId);
}

/**
 * Get the user's timezone.
 */
async function getUserTimezone(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.timezone;
}

/**
 * Update the user's timezone.
 */
async function updateUserTimezone(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('timezone is required');
  }
  await db.users.update(userId, { timezone: value, updatedAt: new Date() });
  return getUserTimezone(userId);
}

/**
 * Get the user's theme.
 */
async function getUserTheme(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.theme;
}

/**
 * Update the user's theme.
 */
async function updateUserTheme(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('theme is required');
  }
  await db.users.update(userId, { theme: value, updatedAt: new Date() });
  return getUserTheme(userId);
}

/**
 * Get the user's newsletter.
 */
async function getUserNewsletter(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.newsletter;
}

/**
 * Update the user's newsletter.
 */
async function updateUserNewsletter(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('newsletter is required');
  }
  await db.users.update(userId, { newsletter: value, updatedAt: new Date() });
  return getUserNewsletter(userId);
}

/**
 * Get the user's twoFactor.
 */
async function getUserTwoFactor(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.twoFactor;
}

/**
 * Update the user's twoFactor.
 */
async function updateUserTwoFactor(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('twoFactor is required');
  }
  await db.users.update(userId, { twoFactor: value, updatedAt: new Date() });
  return getUserTwoFactor(userId);
}

/**
 * Get the user's role.
 */
async function getUserRole(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.role;
}

/**
 * Update the user's role.
 */
async function updateUserRole(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('role is required');
  }
  await db.users.update(userId, { role: value, updatedAt: new Date() });
  return getUserRole(userId);
}

/**
 * Get the user's status.
 */
async function getUserStatus(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.status;
}

/**
 * Update the user's status.
 */
async function updateUserStatus(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('status is required');
  }
  await db.users.update(userId, { status: value, updatedAt: new Date() });
  return getUserStatus(userId);
}

/**
 * Get the user's lastLogin.
 */
async function getUserLastLogin(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.lastLogin;
}

/**
 * Update the user's lastLogin.
 */
async function updateUserLastLogin(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('lastLogin is required');
  }
  await db.users.update(userId, { lastLogin: value, updatedAt: new Date() });
  return getUserLastLogin(userId);
}

/**
 * Get the user's createdAt.
 */
async function getUserCreatedAt(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.createdAt;
}

/**
 * Update the user's createdAt.
 */
async function updateUserCreatedAt(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('createdAt is required');
  }
  await db.users.update(userId, { createdAt: value, updatedAt: new Date() });
  return getUserCreatedAt(userId);
}

/**
 * Get the user's updatedAt.
 */
async function getUserUpdatedAt(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.updatedAt;
}

/**
 * Update the user's updatedAt.
 */
async function updateUserUpdatedAt(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('updatedAt is required');
  }
  await db.users.update(userId, { updatedAt: value, updatedAt: new Date() });
  return getUserUpdatedAt(userId);
}

/**
 * Get the user's plan.
 */
async function getUserPlan(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.plan;
}

/**
 * Update the user's plan.
 */
async function updateUserPlan(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('plan is required');
  }
  await db.users.update(userId, { plan: value, updatedAt: new Date() });
  return getUserPlan(userId);
}

/**
 * Get the user's referralCode.
 */
async function getUserReferralCode(userId) {
  const user = await db.users.findById(userId);
  if (!user) {
    throw new Error('User not found: ' + userId);
  }
  return user.referralCode;
}

/**
 * Update the user's referralCode.
 */
async function updateUserReferralCode(userId, value) {
  if (value === undefined || value === null) {
    throw new Error('referralCode is required');
  }
  await db.users.update(userId, { referralCode: value, updatedAt: new Date() });
  return getUserReferralCode(userId);
}

module.exports = {
  getUserName,
  updateUserName,
  getUserEmail,
  updateUserEmail,
  getUserPhone,
  updateUserPhone,
  getUserAddress,
  updateUserAddress,
  getUserCity,
  updateUserCity,
  getUserCountry,
  updateUserCountry,
  getUserAvatar,
  updateUserAvatar,
  getUserBio,
  updateUserBio,
  getUserLanguage,
  updateUserLanguage,
  getUserTimezone,
  updateUserTimezone,
  getUserTheme,
  updateUserTheme,
  getUserNewsletter,
  updateUserNewsletter,
  getUserTwoFactor,
  updateUserTwoFactor,
  getUserRole,
  updateUserRole,
  getUserStatus,
  updateUserStatus,
  getUserLastLogin,
  updateUserLastLogin,
  getUserCreatedAt,
  updateUserCreatedAt,
  getUserUpdatedAt,
  updateUserUpdatedAt,
  getUserPlan,
  updateUserPlan,
  getUserReferralCode,
  updateUserReferralCode,
};
