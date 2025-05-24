importScripts('https://www.gstatic.com/firebasejs/10.11.0/firebase-app.js');
importScripts('https://www.gstatic.com/firebasejs/10.11.0/firebase-messaging.js');

firebase.initializeApp({
  apiKey: "AIzaSyAy3AEStNYnd-pO-A2XEFmyuu4EgOEDGWs",
  authDomain: "civ6-turn-tracker.firebaseapp.com",
  projectId: "civ6-turn-tracker",
  storageBucket: "civ6-turn-tracker.firebasestorage.app",
  messagingSenderId: "208276184108",
  appId: "1:208276184108:web:2a7983c6a56ef5d3bbc589"
});

const messaging = firebase.messaging();

messaging.onBackgroundMessage(function(payload) {
  const notificationTitle = payload.notification.title;
  const notificationOptions = {
    body: payload.notification.body,
    icon: '/icons/icon-192x192.png' // optional
  };
  self.registration.showNotification(notificationTitle, notificationOptions);
});
